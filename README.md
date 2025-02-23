# Como configurar o Jupyter Notebook no VS Code (com ambiente virtual e kernels)

```markdown
# Configuração de Projeto Python com Ambiente Virtual e Jupyter Notebook

Este guia fornece instruções passo a passo para configurar um projeto Python, criar e ativar um ambiente virtual, instalar o `ipykernel`, configurar um kernel personalizado no Jupyter Notebook e integrar tudo no VS Code.

---

## **Pré-requisitos**

- Python 3.x instalado.
- VS Code instalado.
- Terminal (Linux/Mac) ou Prompt de Comando/PowerShell (Windows).

---

## **Passo a Passo**

### **1. Criar a Pasta do Projeto**

1. Abra o terminal.
2. Crie uma pasta para o projeto:

   ```bash
   mkdir myproject
   ```

3. Navegue até a pasta criada:

   ```bash
   cd myproject
   ```

---

### **2. Criar e Ativar o Ambiente Virtual**

1. Crie um ambiente virtual dentro da pasta do projeto:

   ```bash
   python3 -m venv myenv
   ```

2. Ative o ambiente virtual:

   - No Linux/Mac:

     ```bash
     source myenv/bin/activate
     ```

   - No Windows:

     ```bash
     myenv\Scripts\activate
     ```

3. Quando o VS Code solicitar que você defina o ambiente virtual como padrão para o projeto, clique em **Sim**.

---

### **3. Instalar o `ipykernel`**

Com o ambiente virtual ativado, instale o pacote `ipykernel`:

```bash
pip install ipykernel
```

---

### **4. Criar um Novo Kernel para o Projeto**

Crie um kernel personalizado para o projeto:

```bash
python -m ipykernel install --user --name=myproject
```

---

### **5. Iniciar o Jupyter Notebook**

1. Inicie o Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

2. O terminal exibirá URLs para acessar o Jupyter Notebook. Copie e cole uma delas no navegador.

   Exemplo de saída:

   ```
   To access the notebook, open this file in a browser:
       file:///Users/<seu usuário>/Library/Jupyter/runtime/nbserver-15044-open.html

   Or copy and paste one of these URLs:
       http://localhost:8889/?token=f1ae910e56381c26a62cfb18f83241076bd11d84f7e8e36e
    or https://127.0.0.1:8889/?token=f1ae910e56381c26a62cfb18f83241076bd11d84f7e8e36e
   ```

---

### **6. Configurar o Kernel no VS Code**

1. **Crie um novo Jupyter Notebook**:
   - No VS Code, abra a paleta de comandos (`Cmd + Shift + P` no macOS ou `Ctrl + Shift + P` no Windows/Linux).
   - Digite e selecione: **"Criar: Novo Jupyter Notebook"**.

2. **Selecione o Kernel**:
   - Abra a paleta de comandos novamente.
   - Digite e selecione: **"Notebook: Selecionar Kernel do Notebook"**.
   - Na parte inferior da janela do VS Code, clique em **"Jupyter Server: Local"**.
   - No menu suspenso, insira uma das URLs exibidas no terminal ao iniciar o Jupyter Notebook.

3. **Use o Kernel Personalizado**:
   - Após selecionar o servidor Jupyter, escolha o kernel criado para o projeto (ex.: `myproject`).

---

## **Resumo dos Comandos Principais**

| Etapa                  | Comando                                                                 |
|------------------------|-------------------------------------------------------------------------|
| Criar pasta do projeto | `mkdir myproject`                                                      |
| Criar ambiente virtual | `python3 -m venv myenv`                                                |
| Ativar ambiente virtual| `source myenv/bin/activate` (Linux/Mac) ou `myenv\Scripts\activate` (Windows) |
| Instalar `ipykernel`   | `pip install ipykernel`                                                |
| Criar novo kernel      | `python -m ipykernel install --user --name=myproject`                  |
| Iniciar Jupyter        | `jupyter notebook`                                                     |

---

## **Conclusão**

Seguindo essas etapas, você terá um ambiente de desenvolvimento Python configurado com ambiente virtual, Jupyter Notebook e integração no VS Code. Agora é só começar a programar! 🚀

---