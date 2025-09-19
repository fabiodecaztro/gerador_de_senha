function gerarSenha(tipo) {
  let tamanho = document.getElementById("tamanho").value;
  const resultado = document.getElementById("resultado");

  if (tipo !== "expresso" && (isNaN(tamanho) || tamanho < 4 || tamanho > 40)) {
    resultado.textContent = "Erro: O tamanho deve ser um número entre 4 e 40.";
    resultado.classList.add("error");
    return;
  }

  resultado.classList.remove("error");

  let caracteres = "";
  switch (tipo) {
    case "expresso":
      caracteres =
        "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:,.<>?";
      tamanho = 15; // Força o tamanho para 15 caracteres
      break;
    case "completo":
      caracteres =
        "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:,.<>?";
      break;
    case "alfabetico":
      caracteres = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz";
      break;
    case "alfanumerico":
      caracteres =
        "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
      break;
    case "numerico":
      caracteres = "0123456789";
      break;
  }

  let senha = "";
  for (let i = 0; i < tamanho; i++) {
    senha += caracteres.charAt(Math.floor(Math.random() * caracteres.length));
  }

  resultado.textContent = senha;

  // Copiar para a área de transferência
  navigator.clipboard
    .writeText(senha)
    .then(() => {
      alert(`Senha ${senha} copiada para a área de transferência`);
    })
    .catch((err) => {
      alert("Erro ao copiar senha: ", err);
    });
}
