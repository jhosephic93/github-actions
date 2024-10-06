# Github-Actions
1. Haz click derecho en **Start course** y abre el enlace en una nueva pestaña.
   <br />[![start-course](https://user-images.githubusercontent.com/1221423/218596841-0645fe1a-4aaf-4f51-9ab3-8aa2d3fdd487.svg)](https://github.com/jhosephic93/github-actions/generate)
## Git Configuration

This repository includes a brief overview of Git configuration files and how they adjust its behavior.

### Configuration Files:

1. **/etc/gitconfig**  
   - Affects all users and repositories on the system.
   - Command: `git config --system`.

2. **~/.gitconfig or ~/.config/git/config**  
   - User-specific configuration.
   - Command: `git config --global`.

3. **.git/config (in the repository)**  
   - Applies only to the current repository.

Each file contains settings that Git uses to determine its behavior. You can read or modify these files depending on the level where you want the changes to apply.

### Identity Configuration:

Setting up your identity is crucial for committing changes in Git. You can configure your name and email with the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

If you want to set your identity only for a specific repository (without applying it globally), you should run the following commands at the same level of the repository (without the --global flag):

```bash
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

## GitHub Actions Components

![Components](/img/image01.jpg)

1. **Workflow**: Es un proceso automatizado definido en un archivo YAML. Contiene una serie de pasos que se ejecutan cuando ocurre un evento.

   - Ejemplo: Un workflow que se ejecuta al hacer un push a la rama principal.
2. **Events**: Son desencadenantes que inician la ejecución de un workflow (como un push, pull request, etc.).

   - Ejemplo: on: [push] (inicia cuando se hace push a un repositorio).
3. **Job**: Son conjuntos de pasos que se ejecutan dentro del workflow. Cada job se ejecuta en un runner separado.

   - Ejemplo: Un job que compila el código y corre pruebas.
4. **Runners**: Son máquinas que ejecutan los jobs. Pueden ser auto-hospedados o proporcionados por GitHub.

   - Ejemplo: GitHub-hosted runners que ejecutan Ubuntu o Windows para compilar.
5. **Actions**: Son comandos reutilizables dentro de un workflow. Pueden ser scripts o módulos externos.

   - Ejemplo: actions/checkout@v2 para clonar el repositorio en el runner.

## GitHub Actions MarketPlace

[GitHbu Actions MarketPlace](https://github.com/marketplace?type=actions)
