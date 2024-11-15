# microhackaton19

# Contexto:
Eres el Release Manager de la famosa empresa TuEmpresa, una empresa de comercio electrónico en rápido crecimiento. 
 
# Problema:
Los desarrolladores de TuEmpresa están muy motivados y son muy proactivos a la hora de mejorar las aplicaciones. A veces esta motivación los lleva a realizar despliegues a preproducción o producción de forma autónoma, sin las autorizaciones necesarias y fuera de las fechas acordadas de despliegue, impactando significativamente al funcionamiento de la empresa.  
 
# Solución:
Se propone restringir la ejecución del workflow de despliegue cuando los entornos de destino sean productivos(Pre y Pro). Los despliegues a estos entornos deben ser autorizados por un miembro del equipo de DevOps. Además, únicamente los integrantes del equipo de devops deben poder editar los ficheros que se encuentren en la carpeta .github.
 
# Implementación:
1.	Crear un repositorio en GitHub para almacenar el código fuente de la aplicación de TuEmpresa (puedes reutilizar el de talleres anteriores).
2.	Crear un workflow en el repositorio que tome como parámetro de entrada el entorno de destino, este se debe seleccionar en un desplegable entre los entornos existentes (dev, test, pre, pro). El workflow simplemente imprimirá, con un echo, “Desplegando en el entorno X”
3.	Configura los permisos para que la ejecución del workflow, cuando el entorno de destino sea pre o pro, deba ser aprobada por alguien del equipo de DevOps.

  - Crea una organización de GitHub gratuita y dos equipo dentro de ella.
  - Invita a dos usuarios a la organización, uno a cada equipo.
  - Crear los entornos de GitHub y la protection rule.
  - Crea el archivo CODEOWNER con el equipo que pueda editar en .github.
  - Restringir la forma de mergear código a main, permitiéndolo únicamente a través de Pull Request.
