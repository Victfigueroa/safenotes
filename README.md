### Seguridad Integrada con DevSecOps

**Grupo 5**  
- Juan Villaman  
- Cristóbal Erazo  
- Victor Figueroa  

### ¿Qué aprendiste sobre la diferencia entre SAST, DAST y SCA?
Aprendimos que SAST analiza el código fuente, DAST prueba la app en ejecución y SCA revisa las dependencias. Cada uno detecta riesgos distintos.

### ¿Qué herramientas fueron más fáciles de implementar?
Trivy y Dependency-Check fueron más simples de integrar en GitHub Actions. Su configuración es directa y ofrecen reportes rápidos sin requerir muchos ajustes técnicos.

### ¿Cómo DevSecOps mejora la seguridad sin frenar el desarrollo?
DevSecOps integra seguridad desde el inicio. Automatiza escaneos y pruebas, detectando vulnerabilidades tempranas sin interrumpir el flujo continuo de desarrollo ni ralentizar entregas.

### ¿Qué parte del proceso automatizarías completamente en una empresa?
Automatizaría los escaneos de seguridad en cada push. Esto garantiza que el código que llega a producción fue analizado sin depender de revisiones manuales.


### Presentación explicando cómo aplicarían DevSecOps en un proyecto real

Presentación: Cómo aplicaríamos DevSecOps en un proyecto real
Título: Integrando DevSecOps en el ciclo de vida de SafeNotes

1. Fase de Desarrollo
- Configurar eslint para análisis estático (SAST) desde el inicio.
- Instalar dependencias seguras y verificar con npm audit y OWASP Dependency-Check (SCA).

2. Fase de Integración
- Automatizar npm install, npm test, y escaneos con Trivy en GitHub Actions.
- Configurar GitHub Actions para ejecutar SCA, SAST y pruebas en cada push.

3. Fase de Entorno
- Ejecutar OWASP ZAP (DAST) antes de liberar a producción, explorando rutas críticas como login, registro y dashboard.

4. Fase de Producción
- Usar alertas automatizadas ante nuevas vulnerabilidades de dependencias (Dependabot).
- Incorporar monitoreo de seguridad (WAF, logs, alertas).

Beneficios:
- Seguridad integrada desde el primer commit.
- Automatización continua, sin frenar el desarrollo.
- Menor riesgo en producción, gracias a pruebas preventivas.

### Inicio de Local Host de pagina SafeNote apuntando al puerto 3000
![Captura de pantalla 2025-06-16 213542](https://github.com/user-attachments/assets/3c7f5443-e92b-4150-a6f0-f142a531d97f)
### Analisis ejecutado de ZAP
![Captura de pantalla 2025-06-16 220132](https://github.com/user-attachments/assets/86752f42-52fe-467b-83ac-977628318061)
### Resultados del reporte generado en ZAP
-no se detectaron posibles ataques XSS pero tal como se muestra en la siguiente imagen se presenta un posible peligro en caso de ataque (vulnerabilidad).

![Captura de pantalla 2025-06-16 220143](https://github.com/user-attachments/assets/63483c78-e3a8-4481-b6be-d8ea3c0bff37)
### Resumen de hallazgos de seguridad y solucion sugerida
![Captura de pantalla 2025-06-16 222431](https://github.com/user-attachments/assets/c0a40b55-cc31-439a-af6d-9507f9ee464b)
![Captura de pantalla 2025-06-16 222442](https://github.com/user-attachments/assets/9c31a5eb-0ff8-456a-8e6a-1b8c222c77e7)

