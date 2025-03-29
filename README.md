# 🚀 Desafío 8 – CI/CD con Terraform + GitHub Actions + AWS ☁️

💡 *Prueba de concepto* para automatizar el aprovisionamiento de infraestructura en la nube utilizando **Terraform Cloud**, **GitHub Actions** y **AWS**.

---

## 🛠 Tecnologías Utilizadas

| Herramienta | Descripción |
|-------------|-------------|
| ![Terraform](https://img.shields.io/badge/Terraform-Cloud-blueviolet?logo=terraform) | Gestión de infraestructura como código (IaC). |
| ![GitHub](https://img.shields.io/badge/GitHub-Repositorio-black?logo=github) | Repositorio con versionado y workflows. |
| ![Actions](https://img.shields.io/badge/GitHub%20Actions-CI/CD-blue?logo=githubactions) | Automatización del plan y apply de Terraform. |
| ![AWS](https://img.shields.io/badge/AWS-Proveedor%20Cloud-orange?logo=amazonaws) | Plataforma donde se crean los recursos. |

---

## ⚙️ ¿Cómo funciona?

1. 🚀 El desarrollador hace un *commit* en la rama `main`.
2. 🔁 Se dispara el workflow de **GitHub Actions** definido en `.github/workflows/terraform.yml`.
3. 🧠 Terraform se comunica con **Terraform Cloud** y ejecuta `plan` y `apply` remotamente.
4. ☁️ Se crea un recurso en AWS (por ejemplo, un bucket S3).

---

## 📁 Estructura del Repositorio

```bash
.
├── .github/
│   └── workflows/
│       └── terraform.yml     # Workflow de GitHub Actions
├── main.tf                   # Configuración principal
├── variables.tf              # Variables utilizadas
├── outputs.tf                # Outputs definidos
└── README.md                 # Este archivo
```

🔐 Variables necesarias (en Terraform Cloud)

- AWS_ACCESS_KEY_ID 🔑
- AWS_SECRET_ACCESS_KEY 🔐

⚠️ Asegurate de marcarlas como sensitive y tipo Environment Variable

🧪 Resultado

✔️ Ejecución automatizada validada exitosamente en Terraform Cloud a través de commits en GitHub.
