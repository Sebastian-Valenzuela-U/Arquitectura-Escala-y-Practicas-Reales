# Evidencia: Arquitectura, Escala y Prácticas Reales 🏛️

No buscamos convencerte con aspiraciones; queremos hablar de ingeniero senior a ingeniero senior. Aquí documentamos nuestras decisiones de diseño explícitas, métricas de resiliencia y cómo enfrentamos los datos duros de producción en el día a día.

<img width="550" height="302" alt="02The Beauty of Boring Tech" src="https://github.com/user-attachments/assets/7122003a-6810-45ba-8789-578cf2fa42b6" />


## Filosofía "Boring Technology" y Justificación de nuestro Stack 🛠️

Nuestra elección tecnológica es una decisión deliberada y madura. Utilizamos **Ruby on Rails, PostgreSQL, TypeScript, PHP y Kubernetes**. 

En lugar de perseguir la herramienta de moda, priorizamos la velocidad de entrega y la estabilidad madura frente a una complejidad regulatoria y tributaria que cambia constantemente de forma simultánea en 5 países.

<!-- VIDEO DE JUSTIFICACIÓN DE STACK -->
[▶️ Ver Video: Por qué elegimos Boring Tech](https://drive.google.com/file/d/19sX57zgUO_pkUgP415fEGs_pyfN0Wt4v/view?usp=sharing)

##  Arquitectura y Resiliencia en Escala (El Monolito) 🧩

¿Cómo absorbemos picos transaccionales masivos durante los cierres de nómina de fin de mes en +2 millones de usuarios?

A través de una arquitectura híbrida donde convive nuestro monolito robusto de Rails con microservicios dedicados a dominios específicos. En el frontend, utilizamos **monorepos con librerías de componentes centralizadas** para mantener un tipado estricto. Todo esto respaldado por una infraestructura AWS Multi-Región configurada para máxima alta disponibilidad.

<!-- VIDEO DECISIONES DE DISEÑO Y ARQUITECTURA -->
[▶️ Ver Video: La arquitectura y el Monolito en Buk](https://drive.google.com/file/d/1sNOn8tAPKEXARGmDW0quZK3zYvmkLRgB/view?usp=drive_link)

## Despliegues Estructurados y Cultura de Error 🚢

La responsabilidad de escalar rápido implica fallar de forma segura. Nuestra infraestructura está preparada para desacoplar los *releases* técnicos de los lanzamientos comerciales:
* **Integración Continua (CI/CD)** con una agresiva y alta cobertura de pruebas automatizadas.
* **Feature Flags** integrados como regla de diseño.
* **Blameless Post-Mortems:** Cuando ocurren incidentes en producción, no buscamos culpables; hacemos análisis sistémico de causa raíz centrados únicamente en el aprendizaje del equipo.

## El Cliente en el Centro 👥

Como ingenieros en Buk, asumimos un contrato no escrito: entender *qué, por qué y para quién* construimos. Operamos sistemas de nómina y recursos humanos; sabemos que **cualquier falla en nuestro código impacta directamente en la liquidez financiera de miles de organizaciones y en los hogares de sus colaboradores**. Construimos con esa responsabilidad en mente todos los días.
