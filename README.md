TP01_INFORME PARCIAL_ TEMA DE INVESTIGACIÓN
DATOS GENERALES
Apellidos y nombres estudiante 1: Soto
Quispe, Diego Ulises
Código:
U202214477
Sección:
11980
Asesor metodológico:
Yaneth Charito Vasquez
Olivera
Apellidos y nombres estudiante 2: Gamio
Upiachihua, Brenda Lucía
Código:
U202120344
Sección:
11980
Asesor metodológico:
Yaneth Charito Vasquez
Olivera
Carrera profesional: Ingeniería de Software
Asesor Temático: Yaneth Charito Vasquez Olivera
1 TITULO DEL PROYECTO
Desarrollo de un sistema low-code para automatizar pruebas de seguridad móvil, aplicando
OWASP MASVS (Mobile Application Security Verification Standard), en startups fintech
de Lima.
2 PROBLEMA DE INVESTIGACIÓN
2.1 DESCRIPCIÓN E IMPORTANCIA DEL PROBLEMA / OPORTUNIDAD
Las aplicaciones móviles presenten vulnerabilidades críticas de seguridad a nivel global.
Build38 (2024) documenta que más del 75% de las aplicaciones contienen al menos una
vulnerabilidad de seguridad, mientras que las vulnerabilidades sin parches estuvieron
involucradas en el 60% de las filtraciones de datos. IBM Security (2024) establece que estas
brechas generan costos promedio que alcanzan los 4.88 millones de dólares por incidente.
ResearchDive (2025) reporta que el 83% de las aplicaciones exhiben problemas de seguridad
durante su evaluación inicial, evidenciando que la mayoría llegan a producción sin
verificación rigurosas.
Certo Software (2025) identifica que, en 2024, el 6,3% de los smartphones tenían una
aplicación maliciosa instalada y el 70% del fraude en línea se realiza a través de plataformas
móviles. Asimismo, aproximadamente 24,000 aplicaciones móviles maliciosas son
bloqueada diariamente, reflejando la magnitud constante de amenazas que explotan
vulnerabilidades no detectadas. Lookout (2024) reporta que durante 2024 se publicaron más
1
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
de 160 vulnerabilidades solo en el sistema operativo iOS, donde más del 40% obtuvieron
puntuaciones CVSS superiores a 7, calificándose como de severidad alta o critica.
A nivel regional, América Latina experimenta una escala alarmante en vulnerabilidades de
aplicaciones móviles. Check Point Research (2025a) establece que, durante el primer
semestre de 2025, las organizaciones en la región enfrentan 2,716 ciberataques semanales,
cifra 39% superior al promedio global. Check Point Research (2025b) documenta que la
región experimento el crecimiento más extremo en ciberataques con un incremento del 108%
año tras año en el primer trimestre de 2025. Los informes de amenazas regionales destacan
que el phishing materializado mediante aplicaciones móviles comprometidas representa el
método de ataque predominante, comprometiendo información personal y credenciales de
acceso a millones de usuarios (Certo Software, 2025).
En el contexto peruano, la situación es igualmente crítica. Fortinet, citado por Infobae
(2025a), reporta que durante 2024 se registraron más de 45.5 mil millones de intentos de
ciberataques en el país. FortiGuard Labs documenta que, en el primer semestre de 2025,
sistemas peruanos enfrentaron 36,000 intentos de escaneo por segundo, revelando al nivel
de automatización y persistencia de los adversarios (Infobae, 2025b). ESET, citado por
Infobae (2024), establece que en 2024 se han registrado un millón de detecciones únicas de
phishing en Perú, la cifra más alta en los últimos años. Infobae (2025c) documenta que el
62% de los ciberataques en Perú provino de phishing, aumentando un 9% respecto a 2023.
Múltiples brechas de seguridad han expuesto millones de registros con información sensible,
incluyendo credenciales en texto plano y detalles de transacciones, evidenciando
vulnerabilidades graves en el almacenamiento seguro dentro de aplicaciones móviles.
Se evidencia una brecha critica en la verificación sistemática de seguridad durante el ciclo
de desarrollo de aplicaciones móviles. La insuficiente implementación de controles para
validar el almacenamiento seguro, comunicaciones cifradas y protección de código fuente
permite que vulnerabilidades altamente explotables lleguen a producción, comprometiendo
la confidencialidad e integridad de los datos de usuarios. Build38 (2024) confirma que esta
falta de verificación es un factor determinante en el 60% de las filtraciones de datos
documentadas globalmente.
2.2 ANÁLISIS DEL PROBLEMA
Figura 1
2
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Árbol de problemas sobre causas y efectos de las vulnerabilidades en aplicaciones móviles.
Nota: El presente árbol de problemas ilustra las principales causas y consecuencias asociadas
a las vulnerabilidades críticas de seguridad en aplicaciones móviles. En la parte inferior se
ubican las causas fundamentales como el almacenamiento inseguro de datos, la
comunicación cliente-servidor sin cifrado adecuado y la exposición del código fuente. En la
parte superior se representan los efectos directos e indirectos, tales como la violación de la
confidencialidad de la información, el robo de datos sensibles, las pérdidas económicas, el
deterioro de la reputación corporativa y la pérdida de confianza de los usuarios.
2.3 FORMULACIÓN DEL PROBLEMA
¿Cómo reducir las vulnerabilidades críticas de seguridad en aplicaciones móviles?
La presente pregunta de investigación se enfoca en el problema central identificado: la
persistencia de vulnerabilidades críticas de seguridad en aplicaciones. Estas
vulnerabilidades, documentadas en el árbol de problemas, incluyen almacenamiento
inseguro de credenciales, comunicaciones sin cifrado adecuado y código susceptible a
3
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
ingeniería inversa, generando consecuencias de alto impacto como robo de datos sensibles,
incumplimiento normativo y pérdida de confianza de usuarios.
La interrogante busca determinar los mecanismos efectivos para disminuir la presencia de
estas vulnerabilidades, considerando la necesidad de soluciones accesibles que pueden ser
implementadas con recursos técnicos y económicos limitados, característica común en
diversos contextos de software.
3 CASO DE ESTUDIO
3.1 DATOS GENERALES
El sector financiero tecnológico (Fintech) peruano constituye un ecosistema de alta
relevancia económica caracterizado por su rápido crecimiento y creciente exposición
a desafíos de ciberseguridad. El presente estudio se enfoca en el análisis de múltiples
startups Fintech del ecosistema limeño, adoptando un enfoque sectorial que permite
identificar características comunes, vulnerabilidades recurrentes y necesidades
tecnológicas compartidas por estas empresas emergentes que operan en diversos
segmentos del mercado financiero digital.
Contexto Económico del Sector
Según el Banco Central de Reserva del Perú (2024), el ecosistema Fintech peruano alcanzó
193 empresas locales activas en 2024, operando en diversos segmentos: pasarelas de pagos,
billeteras digitales, préstamos en línea, gestión de finanzas personales e inversiones digitales.
Este sector ha experimentado una expansión notable, con un crecimiento promedio anual del
17% según EY (2024). El ecosistema Fintech procesó 34.9 millones de transacciones con
tarjetas en junio de 20224, representando el 29.3% del total de compras con tarjetas
procesadas en el país (BCRP, 2024).
La evolución del sector refleja una consolidación acelerada. El segmento de pagos y
transferencias lidera con 60 empresas, seguido por préstamos con 54 empresas y gestión
financiera en tercer lugar (EY, 2024). El indicador de Pagos Digitales experimentó un
aumento del 89% en el número de transacciones entre marzo de 2023 y el mismo mes de
2024, impulsado principalmente por la interoperabilidad implementada por el BCRP (EY,
2024).
Marco Normativo y Supervisión
4
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
El sector Fintech peruano opera bajo un marco normativo en evolución, supervisado por la
Superintendencia de Banca, Seguros y AFP (SBS). Los principales instrumentos regulatorios
incluyen:
• Decreto Legislativo N° 1531 (2022): Modifica la Ley General del
Sistema Financiero para facilitar la existencia de entidades 100%
digitales, eliminado requisitos de sede física obligatoria (BCRP, 2024).
• Decreto de Urgencia N° 013-2020: Establece el marco regulatorio para
las actividades Fintech, incluyendo requisitos de registro, cumplimiento
y supervisión (ACOMO, 2024).
• Decreto Legislativo 1665 (2024): Fortalece las facultades del BCPR como
órgano rector del Sistema Nacional de Pagos y amplía la supervisión a
entidades digitales (BCRP, 2024).
• Resolución SBS N° 2429-2021: Reglamenta la realización temporal de
actividades en modelos novedosos (regulatory sandbox) para startups
Fintech (Garrigues, 2023).
La Unidad de Inteligencia Financiera (UIF-Perú) supervisa el cumplimiento de normativas
de prevención de lavado de activos y financiamiento del terrorismo, obligando a las Fintech
a implementar políticas de detección y reporte de actividades sospechosas (ACOMO, 2024).
Base de Clientes y Relevancia Social
El sector Fintech atiende a poblaciones tradicionalmente desatendidas por el sistema
financiero formal. Según el BCRP (2024), el 24.5% de los clientes corresponde a personas
sub-bancarizadas y el 10.2% a personas no bancarizadas. Estos segmentos depositan
creciente confianza en plataformas móviles para acceder a productos de ahorro, crédito y
pagos digitales.
Riesgos de Ciberseguridad en el Sector Financiero
A nivel global, el sector financiero enfrenta amenazas cibernéticas significativas. Según
Speednet (2025), en 2024 el costo promedio de una filtración de datos en el sector financiero
alcanzó 6.08 millones de dólares, superior al promedio global de 4.88 millones de dólares.
Las organizaciones financieras requieren en promedio 168 días para detectar una brecha y
5
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
51 días adicionales para resolverla, permitiendo acceso no autorizado a datos sensibles por
más de siete meses (Neontri, 2025).
Un estudio de ImmuniWeb reveló que el 98% de los 100 principales startups Fintech globales
son vulnerables a ataques web y móviles, mientras que el 97% presentan al menos dos
vulnerabilidades de riesgo medio o alto en sus aplicaciones móviles (Approov, 2023).
Además, el 56% de las aplicaciones móviles Fintech presentan configuraciones incorrectas
graves o problemas de privacidad relacionados con SSL/TLS y endurecimiento inseguro de
servidores web (Approov, 2023).
Las principales amenazas identificadas en el sector incluyen (Fintech Startegy, 2024; SecOps
Solution, 2024):
• Filtraciones de datos: Exposición de información financiera sensible por
explotación de vulnerabilidades.
• Ataques de phishing: El 83% de los sitios de phishing se dirigen
específicamente a dispositivos móviles.
• Vulnerabilidades en APIs: El 92% de las aplicaciones bancarias más
populares contienen credenciales expuestas como claves API (Quokka,
2025).
• Ransomware: El 65% de la industria Fintech experimentó ataques de
ransomware Speednet (2025).
• Ataques DDoS: Interrupciones de servicio que comprometen la
disponibilidad de plataformas.
Desafíos Operativos de las Startups Fintech
Los startups Fintech peruanas enfrentan limitaciones estructurales que dificultan la
implementación de prácticas robustas de ciberseguridad:
• Acceso limitado a financiamiento: El 27.6% de las empresas considera
que la falta de acceso a capital es su principal obstáculo, mientras que el
51% la reconoce como un desafío significativo (BCRP, 2024). En los
primeros tres trimestres de 2024, se registraron solo siete operaciones de
inversión por USD 29 millones, concentrándose USD 28 millones en una
sola Fintech.
6
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
• Barrera bancarias: Las Fintech enfrentan obstáculos para abrir y
mantener cuentas bancarias esenciales para sus operaciones,
fundamentadas en prevención de riesgos, pero carentes de transparencia
(Rextie, 2023).
• Acceso restringido a infraestructura: El acceso limitado a la Cámara de
Compensación Electrónica afecta la capacidad de procesamiento
eficiente de transacciones (Rextie, 2023).
Infraestructura Tecnológica Típica
Los startups Fintech peruanas operan predominantemente sobre arquitecturas cloud-
native, utilizando servicios de proveedores como AWS, Google Cloud Platform y
Microsoft Azure para desplegar aplicaciones móviles nativas (iOS/Android) y
aplicaciones web progresivas. La infraestructura típica comprende:
• Backend: APIs RESTful o GraphQL desplegadas en contenedores
(Docker/Kubernetes).
• Base de datos: Soluciones relacionales (PostfreSQL, MySQL) y NoSQL
(MongoDB, DynamoDB).
• Procesamiento de pagos: Integración con pasarelas como Niubiz, Culqi,
Mercado Pago, Izipay.
• Almacenamiento: Cifrado en reposo (AES-256) y en tránsito (TLS 1.3).
• Autenticación: OAuth 2.0, JWT, autenticación multifactor.
A pesar de estas capacidades tecnológicas, la mayoría de los startups carecen de
equipos dedicados de seguridad (DevSecOps) y dependen de consultorías externas
esporádicas que resultan en validaciones tardías, incompletas y costosas.
Concentración Geográfica y Exposición a Amenazas
Lima concentra la mayor de densidad de startups Fintech del país y, consecuentemente,
la mayor exposición a amenazas cibernéticas. La capital presenta infraestructura de
conectividad móvil densa, alta concentración de servicios financieros digitales y un
ecosistema emprendedor dinámico que la convierte en el epicentro del sector Fintech
nacional.
7
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
3.2 DATOS ESPECÍFICOS
Características Operacionales de las Startups Fintech Estudiadas
El análisis se enfoca en startups Fintech que presentan las siguientes características
estructurales comunes:
Tamaño y Estructura Organizacional
• Equipos técnicos de 5 a 20 desarrolladores
• Ausencia de roles especializados de seguridad (CISO, Security Engineers)
• Presupuestos limitados de ciberseguridad (<5% del presupuesto de TI)
• Dependencia de servicios externos para auditorias de seguridad puntuales
(consultorías que cuestan entre USD 5,000 y USD 15,00 por evolución)
Metodologías de desarrollo
• Implementación de metodologías agiles (Scrum/Kanban) con sprints de 2-4 semanas.
• Prácticas de Integración Continua y Entrega/Despliegue Continua (CI/CD)
implementadas, pero sin integración de seguridad automatizada.
• Despliegues frecuentes en producción (semanales o quincenales).
• Pruebas de seguridad realizadas manualmente o solo previo a lanzamientos mayores.
Funcionalidades Criticas de las Aplicaciones Móviles
Los startups Fintech desarrollan aplicaciones móviles que gestiona operaciones financieras
de alta sensibilidad, incluyendo:
• Billeteras digitales: Almacenamiento de saldos, recarga mediante tarjetas de
crédito/debito, transferencias persona-a-persona (P2P), pagos con código QR
• Plataformas de préstamos: Evaluación crediticia automatizada, firma digital de
contratos, desembolso instantáneo de fondos, gestión de cobranzas.
• Pasarelas de pago: Procesamiento de transacciones con tarjeta, tokenizacion,
integración con comercios electrónicos.
• Gestión de inversiones: Compra/venta de instrumentos financieros, visualización de
portafolios, análisis de rendimiento
• Servicios de remesas: Envió internacional de dinero, conversión de divisas en tiempo
real, seguimiento de transacciones.
8
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Proceso Actual de Desarrollo y Validación de Seguridad
El ciclo de desarrollo tópico de aplicaciones móviles en startups Fintech presenta
deficiencias críticas en materia de seguridad. La siguiente tabla compara el proceso actual
con las mejores prácticas recomendadas.
Tabla 1
Comparación del proceso actual y el proceso seguro en startups Fintech
Fase Proceso Actual (Sin herramientas
automatizadas)
Proceso Ideal (Con
automatización de seguridad)
Fase 1:
Desarrollo
(Semanas 1-8)
- Desarrollo de
funcionalidades sin
consideraciones explicitas de
seguridad
- Sin análisis estático de código
automatizado
- Sin revisión de permisos o
configuraciones de seguridad
durante el desarrollo
- Almacenamiento de
credenciales sin validación
criptográfica
- Análisis estático de
código integrado de IDE
- Validación automática
de prácticas seguras
- Escaneo de
dependencias
vulnerables
- Verificación de
implementaciones
criptográficas
Fase 2: Pruebas
Funcionales
(Semanas 9-
10)
- Foco exclusivo en
funcionalidad (casos de uso
exitosos y errores
funcionales)
- Sin pruebas de seguridad
especifica (penetration
testing, fuzzing)
- Sin validación contra
estándares como OWASP
MASVS.
- Pruebas de seguridad
automatizadas en
pipeline CI/CD
- Validación contra
OWASP MASVS
- Análisis dinámico de
aplicaciones (DAST)
- Pruebas de
interceptación de trafico
Fase 3:
Auditoría
Externa
(Semana 11, si
se realiza)
- Contratación eventual de
consultoras de seguridad
(costo: USD 5,000-15,000)
- Pruebas manuales por
expertos (2-5dias)
- Identificación tardía de
vulnerabilidades cuando el
código está cerca de
producción
- Tiempo de esta remediación
limitado, priorizando solo
fallas criticas
- Auditorias
complementarias sobre
código pre-validado
- Enfoque en validación
de arquitectura y lógica
de negocio
- Revisión de controles de
seguridad específicos
- Recomendaciones
estratégicas de
ciberseguridad
9
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Fase 4:
Despliegue
(Semana 12)
- Lanzamiento con
vulnerabilidades de severidad
media/baja sin remedias.
- Sin monitoreo continuo de
seguridad post-despliegue
- Sin proceso de actualización
rápido ante aparición de
nuevas vulnerabilidades.
- Despliegue con
validación completa de
seguridad
- Monitoreo continuo de
amenazas
- Actualización
automatizada ante CVEs
- Respuesta rápida a
incidentes
Nota: Esta tabla resume las diferencias entre el desarrollo tradicional y el desarrollo con
seguridad integrada. Permite observar como la automatización de pruebas y validación
continua reducen errores fortalecen la protección desde las primeras fases.
Vulnerabilidades Criticas Identificadas
El análisis del proceso de desarrollo actual revela vulnerabilidades recurrentes que exponen
a los startups Fintech a riesgos significativos. La siguiente tabla detalle las principales
vulnerabilidades, sus causas raíz y consecuencias:
Tabla 2
Principales vulnerabilidades en aplicaciones móviles Fintech
Vulnerabilidad Causa Raíz Manifestación Técnica Consecuencia
Almacenamiento
Inseguro de
Credenciales
Falta de
validación
automatizad
a de
implementa
ciones
criptográfic
as durante el
desarrollo
- Datos almacenados
sin cifrados o con
cifrado débil
- Tokens de sesión en
SharedPreferences
(Android) sin
protección
- Credenciales en
UserDefaults (iOS)
en texto plano
- Claves API
embebidas en código
fuente
- Extracción de
credenciales
mediante
acceso físico
al dispositivo
- Compromiso
de cuentas
mediante
malware
- Robo de
identidad
financiera
Comunicación
Cliente-Servidor
sin Cifrado
Adecuado
Ausencia de
pruebas
automatizad
as de
interceptaci
- Transmisión de datos
en texto plano
- TSL mal configurado
(configuraciones
antiguas)
- Intercepción
de datos
financieros en
redes WIFI
pública
10
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
ón de tráfico
durante
CI/CD
- Sin validación de
certificados
SSL/TLS
- Aceptación de
certificados
autofirmados
- Ataques de
Man in-the-
Middle
- Exposición de
credenciales
en transito
Código
Susceptible a
Ingeniera Inversa
Sin
herramienta
s de
ofuscación
ni análisis de
exposición
de secretos
- Lógica de negocio
expuesta
directamente en el
código
- Claves API extraíbles
mediante de
compilación
- Endpoints internos
revelados en binarios
- Algoritmos
propietarios sin
protección
- Explotación de
APIs internas
- Bypass de
validaciones
de negocio
- Clonación de
aplicaciones
- Fraude
mediante
ingeniería
inversa
APIs sin
Autenticación
Robusta
Falta de
pruebas de
seguridad en
endpoints
durante el
desarrollo
- APIs accesibles sin
tokens de
autenticación
- Validación
insuficiente de
permisos
- Exposición de datos
sensibles en
respuestas
- Falta de rate limiting
- Acceso no
autorizado a
datos de
usuarios
- Exfiltración
másica de
información
- Ataques de
denegación de
servicio
(DOS)
Gestión
Inadecuado de
Sesiones
Sin
validación
automatizad
o de ciclos
de vida
sesión
- Tokens de sesión sin
expiración
- Sesiones activas
después de logout
- Tokens predecibles o
reutilizables
- Secuestro de
sesiones
(sesión
hijacking)
- Acceso no
autorizado
persistente
Nota: La tabla identifica las fallas más críticas detectadas en los sistemas móviles
financieros. Explica brevemente su origen, como se manifiestan en el entorno técnico y el
impacto que generan sobre la seguridad y la confianza de usuarios.
Brecha entre Necesidades y Soluciones Disponibles
Los startups Fintech requieren una solución que considere sus restricciones operacionales
especificas:
11
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Requisitos Identificados
• Accesibilidad: Interfaz low-code que no requiera expertos en seguridad para su
operación
• Costo: Alternativa económica a consultorías externas recurrentes (reducción del 70-
80% del costo)
• Integración: Compatibles con pipelines CI/CD existentes (Github Actions, GitLab
CI, Jenkins)
• Velocidad: Resultados en minutos/horas en lugar de días, ajustándose a ciclos agiles
• Cobertura: Validación automatizada de estándares internacionales (OWASP
MASVS)
• Educación: Reportes explicativos que capaciten a equipos en remediación de
vulnerabilidades.
Análisis de Alternativas Actuales
• Consultorías tradicionales: Costo prohibitivo (USD 5,000-15,000 por evaluación),
identificación tardía de vulnerabilidades, dependencia de disponibilidad de expertos
externos
• Herramientas comerciales avanzadas: Complejidad técnica alta, requieren
especialistas en seguridad, costos de licenciamiento elevados (USO 20,000-50,000
anuales).
• Herramientas open-source: Curva de aprendizaje pronunciada, configuración
compleja, sin reporte empresarial, resultados difíciles de interpretar para equipos no
especializados.
4 PROPUESTA DE MEJORA COMO SOLUCIÓN DE INVESTIGACIÓN
4.1 DESCRIPCIÓN DE LA PROPUESTA
Definición de la mejora
La propuesta consiste en desarrollar un sistema automatizado de análisis de seguridad para
aplicaciones móviles Flutter que integra tres técnicas complementarias: Análisis Estático de
código (SAST), Análisis Dinámico en Ejecución (DAST) y validación contra el estándar
OWASP Mobile Application Security Verification Standard (MASVS). El sistema utiliza una
12
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
interfaz low-code que permite a desarrolladores sin especialización en seguridad realizar
evaluaciones profesionales de forma automatizada e integrada al ciclo de desarrollo.
Según el Fintech Radar Perú 2024, el ecosistema Fintech peruano está conformado por 346
startups activas (Finnosummit, 2024), enfrentando limitaciones de recursos donde el 27.6%
identifica la falta de capital como obstáculo principal (BCRP, 2024). El diagnostico
identifico que el 97% de las aplicaciones móviles Fintech contienen al menos dos
vulnerabilidades de riesgo medio o alto, mientras que menos del 35% implementan pruebas
de seguridad automatizadas, requiriendo 15-30 días para detectar vulnerabilidades
manualmente (Approov, 2023).
Modelo conceptual de la Solución
Figura 1
Modelo conceptual del sistema de verificación de seguridad móvil
13
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Nota: La figura representa el flujo funcional del sistema propuesto, desde la aplicación móvil
flutter hasta la generación de reportes CI/CD, integrando módulos del análisis SAST, DAST
y validación MASVS para fortalecer la seguridad del software.
Componentes Principales
Modulo SAST: Examina código Dart y binarios APK/IPA sin ejecutar la aplicación,
detectando credenciales sin cifrado en SharedPrefereneces/UserDefaults, claves API
embebidas y criptografía débil. Proporciona ubicación exacta (archivo/línea) con ejemplos
de remediación en Flutter conforme a controles MASVS-STORAGE y MASVS-CRYPTO
(OWASP Foundation, 2024).
Modulo DAST: Ejecuta la aplicación en emuladores instrumentos con proxy MITM,
validando configuración TLS 1.2+, certificate pinning y ausencia de transmisión en texto
plano conforme a MASVS-NETWORK (OWASP Foundation, 2024). Genera evidencia
visual de interceptación y configuraciones correctivas.
Modulo MASVS: Mapea hallazgos SAST/DAST a controles OWASP Mobile Application
Security Verification Standard v2.1.0 (STORAGE, CRYPTO, AUTH, NETWORK,
PLATFORM, CODE, RESILIENCE), generando reportes de cumplimiento para auditorias
(OWASP Foundation, 2024).
Alcance y Exclusiones
Alcance:
• Aplicaciones móviles desarrolladores en Flutter (iOS/Android)
• Startups Fintech del ecosistema limeño con equipos de 5-20 desarrolladores
• Controles OWASP MASVS v2 niveles L1 y L2 (STORAGE, CRYPTO,
NETWORK, CODE)
• Integración nativa con sistemas CI/CD: Github Actions, GitLab CI, Jenkins
• Análisis automatizado de código fuente Dart y binarios compilados (APK/IPA)
• Pruebas dinámicas en emuladores Android API 30+ e iOS 15+
Exclusiones (Fuera de alcance en esta etapa)
• Aplicaciones nativas puras en Swift/Kotlin sin framework Flutter
14
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
• Aplicaciones web progresivas (PWA) o hibridas en otros frameworks (React Native,
Ionic).
• Pruebas de penetración manuales avanzadas que requieren expertos en seguridad
• Análisis de seguridad de infraestructura backend, servidores o servicios cloud
• Monitoreo de seguridad en producción mediante RASP (Runtime Application Self-
Protection) o WAF (Web Application Firewall)
• Controles OWASP MASVS L3 (anti-reversing avanzado) que requieren técnicas de
ofuscación complejas
4.2 CORRESPONDENCIA CON CAUSAS PRIORIZADAS DEL ÁRBOL DE
PROBLEMAS
El árbol de problemas identifico tres causas principales de vulnerabilidades en aplicaciones
móviles. La propuesta aborda directamente cada causa mediante mecanismos automatizados
de detección y remediación guiada.
Causa 1: Almacenamiento Inseguro de Datos Sensibles
Problema identificado: Credenciales, tokens y datos financieros almacenados sin cifrado
en dispositivos móviles.
Solución mediante SAST:
• Detecta almacenamiento de credenciales en SharedPreferences/UserDefaults sin
protección.
• Identifica algoritmos criptográficos obsoletos (DES, MD5, SHA-1)
• Marca persistencia innecesario de datos sensibles que podrían mantenerse solo en
memoria
• Proporciona código de ejemplo usando flutter_secure_storage conforme a MASVS-
STORAGE-1 (OWASP Foundation, 2024)
Metas de detección
• Cobertura: 85-90% de casos mediante análisis de patrones sintácticos y semánticos
• Ubicación: Archivo y línea exactos del código problemática
• Tiempo: Reducción de 15-30 días (proceso manual) a menos de 10 minutos (análisis
automatizado)
15
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
La meta del 85-90% se fundamenta en capacidades documentadas del análisis estático para
detectar patrones de almacenamiento inseguro, con limitaciones únicamente en casos de
ofuscacion avanzada o generación dinámica de claves.
Causa 2: Comunicación Cliente-Servidor sin Cifrado Adecuado
Problema identificado: Transmisión de datos mediante conexiones con TSL/SSL
incorrectamente implementado.
Solución mediante DAST
• Intercepta trafica mediante proxy MITM en emulador instrumentado
• Valida uso de TSL 1.2+ y suites de cifrado seguras conforma a MASVS-
NETWORK-1 (OWASP Foundation, 2024)
• Detecta aceptación de certificados autofirmados o sin validación
• Verifica implementación de certificate pinning según MASVS-NETWORK-2
Metas de detección
• Cobertura: 100% de endpoints utilizados durante pruebas de ejecución
• Precisión: 90-95% de vulnerabilidades de comunicación detectadas
• Evidencia: Capturas de trafica interceptado con configuraciones correctivas
específicas.
La meta del 90-95% se basa en la naturaleza determinística del análisis dinámico de red
donde la interceptación activa confirma vulnerabilidades con certeza, con limitaciones solo
en flujos no activos durante pruebas.
Causa 3: Código Susceptible a Ingeniería Inversa
Problema identificado: Lógica de negocio y secretos expuestos en código cliente facilitando
clonación y explotación.
Solución mediante SAST
• Detecta claves API mediante analisis de entropía y patrones regex especializados
• Identifica endpoints internos expuestos en código cliente
• Señala logica de negocio critica que debería ejecutarse en servidor conforme a
MASVS-CODE-2 (OWASP Foundation, 2024).
16
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
• Recomienda refactorización arquitectónica y gestión remota de secretos segun
MASVS-STORAGE-2
Metas de detección
• Cobertura: 75-80% de secretos embebidos mediante análisis de entropía combinado
con patrones
• Impacto: Reduccion aproximada del 60% de superficie de ataque por ingeniería
inversa
• Recomendaciones: Arquitectónicas para mover validaciones críticas al backend
La meta del 75-80% refleja limitaciones conocidas del análisis estático en casos donde
secretos están cifrados en el código o se construyen dinámicamente mediante concatenación
compleja.
4.3 NIVEL DE APORTE E INNOVACIÓN
No existe actualmente una herramienta que combine análisis estático (SAST), análisis
dinámico (DAST) y validación automatizada contra OWASP MASVS v2 en una interfaz
low-code optimizada específicamente para Flutter y diseñada para startups con recursos
limitados. La integración de tres técnicas complementarías elimina la necesidad de operar
múltiples herramientas desconectadas, mientras que la correlación inteligente de hallazgos
reduce significativamente los falsos positivos característicos de soluciones basadas en una
única técnica de análisis.
Aporte técnico: Empaquetamiento de capacidades de análisis profesional (datos, red,
secretos) en plataforma única con detección precisa y guías de remediación específicas para
Flutter/Dart.
Aporte metodológico: (DevSecOps sin fricción): Transforma la seguridad de una actividad
esporádica reactiva (auditorías externas puntuales costosas) en un proceso continúo
automatizado integrado nativamente al ciclo de desarrollo, sin imponer sobrecarga
significativa en tiempos de build mediante optimizaciones de análisis incremental.
Aporte contextual (ecosistemas Fintech peruano): Diseñado específicamente para las
características operacionales de startups Fintech en Lima: equipos pequeños (5-20
desarrolladores), ausencia de roles especializados en seguridad, presupuestos limitados
17
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
documentados (27.6% sin acceso a capital), y adopción del stack Flutter como tecnología
predominante de desarrollo móvil.
Tabla 3
Comparación de Características de Herramientas de Seguridad Móvil
Características MobSF Burp Suite NowSecure Propuesta
No incluido Incluido
completamente
SAST completo Incluido
completamente
DAST completo No incluido Incluido
completamente
No incluido No incluido Incluido
completamente
Incluido
completamente
Incluido
completamente
Incluido
completamente
Validación
MASVS v2
automatizada
Incluido
completamente
Interfaz low-
code
No incluido No incluido Incluido
parcialmente
Incluido
completamente
Optimización
Flutter
específica
Incluido
parcialmente
Incluido
parcialmente
Incluido
parcialmente
Incluido
completamente
Integración
CI/CD nativa
Incluido
parcialmente
Incluido
parcialmente
Incluido
completamente
Incluido
completamente
Reportes
pedagógicos
No incluido No incluido Incluido
parcialmente
Incluido
completamente
Costo para
startups
Gratuito (sin
soporte)
USD
449/usr/año
>USD 60k/año Accesible
Curva de
aprendizaje
Alta (semanas) Alta (semanas) Media (días) Baja (horas)
Soporte en
español
No incluido No incluido Incluido
parcialmente
Incluido
completamente
Nota: Esta tabla compara las principales herramientas de análisis de seguridad móvil
disponibles en el mercado con la propuesta de solución desarrollada en el presente trabajo.
Se evalúan criterios clave como la cobertura de técnicas de análisis (SAST, DAST),
validación automatizada contra el estándar OWASP MASVS, facilidad de uso mediante
interfaz low-code, optimización específica para Flutter, integración con pipelines CI/CD,
generación de reportes pedagógicos, costos accesibles y soporte en español.
Ventaja Diferenciadoras
• Accesibilidad sin sacrificar profundidad técnica:
18
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
La interfaz low-code permite que desarrolladores sin información
especializada en seguridad puedan configurar y ejecutar análisis profesionales
cumpliendo estándares OWASP, mientras mantiene la profundidad técnica
necesaria para identificar vulnerabilidades complejas que requieren correlación
entre múltiples fuentes de evidencia (SAST + DAST).
• Optimización específica para Flutter:
A diferencia de herramientas genéricas que soportan múltiples frameworks con
profundidad limitada, la propuesta está optimizada para el stack Flutter/Dart,
incluyendo detección de patrones específicos de vulnerabilidades
característicos de este framework (uso incorrecto de SharedPreferences,
problemas con secure_storage) y ejemplos de remediación en código Dart
idiomático.
• Modelo de costos orientado a startups:
El modelo de negocio propuesto considera las restricciones presupuestarias
documentadas del sector Fintech peruano (27.6% identifica falta de capital
como obstáculo principal según BCRP 2024), ofreciendo alternativa
económicamente viable frente a consultorías tradicionales que cuestan USD
5000-15000 por evaluación puntual o plataformas empresariales que superan
los USD 60000 anuales de licenciamiento.
4.4 PLAN DE IMPLEMENTACIÓN
Fases Principales:
Fase 1: Levantamiento y Definición de Requisitos (2 semanas)
Entrevista semi-estructuradas con 8-10 startups Fintech representativas del ecosistema
limeño para priorizar controles MASVS v2 críticos según necesidades reales del
sector, definir criterios de éxito medibles y acordar participación en pruebas piloto con
compromiso de retroalimentación continua.
Fase 2: Diseño de Arquitectura (2-3 semanas)
Diseño detallado de arquitectura de microservicios para módulos
SAST/DAST/MASVS, especificación de APIs internas RESTful, esquema de base de
datos para almacenamiento histórico de resultados, estrategia de integración con
19
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
GitHub Actions/GitLab CI/ Jenkins mediante webhooks, y diseño de interfaz de
usuario low-code con wireframes validados.
Fase 3: Desarrollo del Prototipo (6-8 semanas)
Desarrollo iterativo organizado en sprints de 2 semanas:
• Sprints 1-2 (Módulo SAST): Parser de código Dart, reglas de detección de
almacenamiento inseguro, identificación de secretos mediante regex +
entropía, generación de reportes con ubicación exacta.
• Sprints 3-4 (Módulo DAST): Configuración de emuladores Android/iOS
instrumentados, implementación de proxy MITM, validación de TLS/SSL,
generación de evidencia visual.
• Sprints 5-6 (Módulo MASVS): Mapeo automático a controles OWASP
MASVS v2, motor de correlación SATS-DAST, sistema de priorización por
severidad, reportes diferenciados técnico/ejecutivo.
Fase 4: Integración a CI/CD (2 semanas)
Desarrollo de plugins nativos para GitHub Actions (YAML workflow), GitLab CI
(configuración.gitlab-ci.yml) y Jenkins (Jenjinsfile), con ejecución automática por
commit/pull request, sistema de bloqueo de despliegue ante vulnerabilidades críticas
sin resolver, y generación de artefactos de build con reportes de seguridad adjuntos.
Fase 5: Prueba Piloto y Ajustes (4-6 semanas)
Despliegue controlado en 3-4 startups fintech colaboradoras, ejecución de análisis en
aplicaciones reales de producción, medición de indicadores clave (tiempo, falso
positivos, vulnerabilidades detectadas), sesiones semanales de retroalimentación con
equipos de desarrollo, calibración de reglas de detección mediante machine learning y
ajuste de umbrales, mejora iterativa de mensajes de error y guías de remediación
basada en feedback cualitativo.
Fase 6: Documentación y Preparación para Adopción (2 semanas)
Redacción de documentación técnica completa (arquitectura, APIs, configuración),
creación de guías de usuario paso a paso con capturas de pantalla, desarrollo de
tutoriales en video de 5-10 minutos, elaboración de plantillas de políticas de seguridad
20
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
adaptadas a fintech, y definición de línea base de controles mínimos recomendados
según perfil de riesgo.
Indicadores de Éxito y Criterios de Aceptación
Tabla 4
Indicadores Clave de Desempeño (KPIs)
Indicador Meta Criterio de Aceptación Método de
Medición
Tiempo de
análisis CI/CD
<=15
minutos
90% de análisis completados
dentro del objetivo sin timeout
Logs de ejecución
con timestamps
Secretos en
producción
0 secretos
críticos
Bloqueo automático si SAST
detecta claves API/token sin
justificación aprobada
Análisis de
binarios pre-
producción
Comunicaciones
seguras
100% TLS
1.2+
DAST no logra interceptar
tráfico sensible en pruebas
MITM
Reportes de
análisis dinámico
Correciones
aplicadas
>=80% en
2 semanas
Vulnerabilidades críticas/altas
remediadas dentro de 1 sprint
Comparación
reportes
antes/después
Adopción
sostenida
>=90% de
commits
Sistema ejecuntándose
automáticamente durante
semanas 4-8 del piloto
Logs de actividad
CI/CD
Falsos positivos <=15% Hallazgos confirmados por
correlación SAST-DAST o
validación de desarrollador
Encuestas +
sistema de reporte
Nota: Los indicadores están alineados con mejores prácticas de DevSecOps
documentadas y serán validados empíricamente durante la fase piloto. Los criterios de
aceptación podrán ajustarse según restricciones operacionales específicas de cada
startup participante.
5 ANTECEDENTES DE LA PROPUESTA
Romdhana et al. (2023) presentan RONIN, un sistema con Deep Reinforcemente Learning
para explotar vulnerabilidades ICC en Android. En 1500 aplicaciones de Google Play genero
tres veces más exploits que herramientas previas, mostrando avances en automatización. Sin
embargo, se centra en explotación y no en validación preventiva, lo que deja pendiente el
desarrollo de soluciones orientadas a la protección temprana de aplicaciones móviles.
Ebbers et al. (2024) desarrollan Gran Theft API, un método de adquisición forense de datos
vehiculares en la nube mediante APIs. Analizaron 23 aplicaciones y verificaron acceso a
datos de seis fabricantes como BMW y Tesla. Aunque evidencian riesgos de exposición de
21
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
datos sensibles, sun enfoque es reactivo y limitado al ámbito vehicular, sin importar
mecanismos de validación preventiva en aplicaciones móviles de otros sectores.
Onik et al. (2024) introducen PyShot, herramienta en Python para extraer datos de la nube
de Progressive Snapshot. Confirmaron precisión en velocidad y ubicación, además de
informacion oculta como maniobras peligrosas. Incluso reconstruyeron un caso de “hit-and-
run” con coordenadas y tiempos. Su aporte es forense y post-incidente, por lo que no
responde a la necesidad de validar la seguridad de aplicaciones antes de su uso.
Shi et al. (2025) proponen un modelo multidimensional que combina análisis estático,
dinámico y expectativas de usuario. Alcanzaron 97.27% de precisión en la detección de
comportamientos maliciosos en aplicaciones reales. Aunque integran Técnicas de forma
efectiva, su orientación es hacia la clasificación de malware y no hacia la validación de
estandares de seguridad en entorno de desarrollo continuo.
Duy & Cam (2025) presentan uitObfAMC, un marco de clasificacion de malware Android
ofuscado basado en imágenes multi-caracteristicas y CNNS. Entrenaron con 34, 619 APKs
aplicando 20 técnicas de ofuscación y lograron 95.23% de precisión en clasificación binaria.
A pesar de su eficacia, requiere infraestructura de cómputo intensiva y se limita a la detección
de malware, sin aportar soluciones prácticas para validación preventiva en contextos con
menos recursos.
Dawood et al. (2024) revisan el impacto de DNS over HTTPS (DoH) en ciberseguridad.
Identifican beneficias en privacidad, pero también riesgos como perdida de visibilidad para
sistemas de detección y uso de DoH para tunneling malicioso. Aunque relevante en el ámbito
de redes, no aborda la validación de aplicaciones móviles, lo que lo convierte en un
antecedente complementarios pero insuficiente frente a los retos de seguridad de software.
Palutla et al. (2025) ofrecen una revisión integral de Vulnerability Assement and Penetration
Testing (VAPT) en Android. Señalan que más del 85% de aplicaciones móviles presentan
vulnerabilidades comunes según OWASP Mobile Top 10. Sin embargo, no plantean
soluciones prácticas accesibles a equipos pequeños ni integración automatizadas, lo que
limite su aplicación en escenarios reales de desarrollo ágil.
Amalfitano et al. (2025) demuestran la eficacia de las pruebas metamórficas GUI, detectando
159 vulnerabilidades en 108 de 163 aplicaciones evaluadas. Sin embargo, herramientas
existen como MobSF y Burp Suite presentan limitaciones criticas para entornos de startups,
22
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
complejidad y técnica elevada, costos prohibitivos y falta de integración especifica con
Flutter, dejando un vacío en soluciones accesibles que aborden integralmente los estándares
OWASP MASVS requeridos en el sector Fintech.
Karayel y Saygili (2025) demuestran mediante un estudio con 875 usuarios que los factores
de la Protection Motivation Theory explican el 71% de la varianza en el comportamiento de
seguridad móvil. Revelando diferencias claves entre sistemas operativos como el impacto
del costo respuesta solo en usuarios iOS. Si bien existe herramientas técnicas de seguridad,
estas no abordan las diferencias conductuales específicas de cada plataforma identificadas
en el estudio, dejando un vacío critico en soluciones que integran el factor humano con la
evaluación técnicas, lo que justifica que investigaciones posteriores para desarrollar
enfoques integrales en ciberseguridad móvil.
Karayel y Saygili (2025) identifica que el “costo de respuesta” solo es relevante para usuario
de iOS, evidenciando la necesidad de estrategias diferenciadas por sistema operativo. Frente
a las soluciones genéricas actuales, que ignoran estas diferencias psicológicas, tu tesis
adquiere valor al proponer un modelo personalizado que, basado en estos hallazgos, supera
la limitación del enfoque única y aumenta la efectividad de las intervenciones en seguridad
móvil.
Zhang et al. (2025) indican que el malware evasivo en Android sigue siendo una amenaza
importante, ya que una gran parte de las muestras detecta emuladores o manipula como
Kaspersky Research Sandbox o VPBox, la mayoría de los métodos solo examina la capa
Java y deja de fuera el código nativo, lo que reduce su eficacia. El estudio evidencia la falta
de soluciones completas que combinen distintas capas de análisis para evaluar la seguridad
movil de forma práctica y confiable.
Senanayake et al. (2024) presenta un sistema de detección de vulnerabilidades en código
fuente Android basado en redes neuronales federadas con blockchain y técnicas de
inteligencia artificial explicable (XAI). Entrenado sobre el dataset LVDAndro, el modelo
alcanza una precisión del 96% y un F1-score de 0.96 en clasificación binaria, y 93% de
precisión en clasificación multiclase por categorías CWE. Esta propuesta aporta valor al
enfocarse en validación preventiva ligera y accesible para desarrolladores en etapas
tempranas del ciclo vida.
23
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Xiang et al. (2025) propone una herramienta de análisis estático de flujos de taint en Android
que mejora la precisión al incorporar grafos etiquetados y análisis finos de estructuras tipo
List. Este trabajo complementa nuestro trabajo de investigación al enfocarse en validación
de seguridad desde el código fuente, en tiempo real y dentro del entorno de desarrollo.
Smmarwar et al. (2024) ofrece una revisión exhaustiva de técnicas de detección de malware
en Android, agrupadas en tres categorías: selección de características, modelos de ML y
aprendizaje profundo (DL). Este trabajo aporta un valor al ofrecer una solución práctica,
integrada y orientada a prevenir vulnerabilidades antes del despliegue.
Eichhorn & Pugliese (2024) analiza 16 relays inteligentes de 9 marcas y 6 aplicaciones
Android, identificando artefactos locales, en la nube y en tráfico de red. Esta propuesta se
diferencia de la nuestra al centrarnos en la detección temprana de vulnerabilidades en el
código fuente Android, antes de que se convierta en incidentes forenses.
Madhushanie et al. (2025) realiza una revisión sistemática de técnicas para detectar
vulnerabilidades de privacidad de tiempo real durante el desarrollo del software. Clasifica
las soluciones en herramientas integradas en IDEs. Esta propuesta aporta valor al enfocarse
en validación preventiva específica para Android, con bajo costo computacional y alta
adaptabilidad.
R. Arikkat et al. (2025) demuestra que es posible mapear aplicaciones Android con los TTPs
del marco MITRE ATT&CK de forma automatizada y altamente precisa. Su modelo logró
un Jaccard Similarity de 0.9893 para Tácticas y 0.9753 para Técnicas. Esta propuesta aporta
validación en viabilidad de automatizar la atribución de técnicas de ataques a partir de
características estáticas de apps.
Josephine et al. (2025) este estudio desarrolla modelos de clasificación para detectar adware,
malware y aplicaciones benignas en Android, utilizando técnicas como Random Forest y
XGBoost. El modelo final alcanzó una precisión de 92.51% al integrar características del
tráfico de red. Esta propuesta se diferencia al centrarse en la detección temprana de
vulnerabilidades durante el desarrollo, sin requerir ejecución ni monitoreo de tráfico.
Zhang et al. (2025) realiza un análisis empírico de herramientas para detectar bibliotecas de
terceros en Android, fundamentales para la seguridad de la cadena de suministro. Se encontró
que el 57% de las aplicaciones contienen TLPs y que hasta el 60% del código proviene de
24
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
estas bibliotecas. La propuesta aporta valor al enfocarse en la seguridad desde el código
fuente, antes de que las bibliotecas sean integradas o desplegadas.
Taheri et al. (2024) analiza cómo los atacantes pueden usar técnicas de privacidad diferencial
para generar ejemplos adversarios que comprometan clasificaciones de malware en Android.
Se proponen dos ataques que mejora la precisión hasta en 45.46% frente ataques. Esta
propuesta integra validación preventiva en entornos CI/CD, sin depender de modelos
complejos ni infraestructura intensiva.
6 MOTIVACIÓN
La motivación para desarrollar este sistema automatizado de análisis de seguridad móvil se
fundamenta en los resultados concretos y cuantificables que se espera obtener,
transformando la seguridad de aplicaciones móviles de un costo prohibitivo en una inversión
accesible con retorno medible para el ecosistema Fintech peruano.
Resultados Esperados con Métricas Específicas
1. Reducción Significativa de Costos Operativos
Situación actual: Los startups Fintech que contratan consultorías de seguridad enfrentan
costos de USD 5000-15 000 por evaluación puntual, totalizando USD 65 000-390 000
anuales considerando 13-26 despliegues por año, monto prohibido para el 40% de
startups con ingresos menores a USD 500 000 anuales (Finnosummit, 2024).
Resultado esperado: Reducción del 85-90% en costos de validación de seguridad,
pasando a USD 8000-12 000 anuales por licencia de plataforma, generando ahorro de
USD 53 000-378 000 por startup anualmente. ROI: recuperación de inversión en el
primer sprint de uso (2-4 semanas).
2. Reducción Drástica del Tiempo de Detección de Vulnerabilidades
Situación actual: El proceso manual requiere 15-30 días desde el despliegue hasta
identificación de vulnerabilidades, periodo durante el cual la aplicación permanece
expuesta con fallas críticas activas en producción.
Resultado esperado: Reducción del 99.65% en tiempo de detección, pasando de 15-30
días (360-720 horas) a menos de 15 minutos mediante análisis automatizado integrado
25
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
en pipeline CI/CD. Detección temprana en fase de desarrollo antes de merge a
producción.
3. Incremento de Cobertura de Validación de Seguridad
Situación actual: Menos del 35% de startups Fintech implementan pruebas de seguridad
automatizadas (Approov, 2023), y las auditorías externas validan únicamente 1-2
despliegues anuales, dejando sin analizar el 90-95% del código desplegado.
Resultado esperado: Incremento de cobertura del 10% al 100% de código desplegado,
validando automáticamente todos los commits y pull requests (200-500+ validaciones
anuales). Validación del 100% de endpoints de comunicación cliente-servidor mediante
DAST.
4. Reducción del Tiempo Medio de Remediación (MTTR)
Situación actual: El MTTR promedio es de 45-60 días (compresión de reporte: 5-7 días,
priorización: 7-14 días, desarrollo: 14-21 días, testing: 7-10 días, redespliegue: 3-5 días),
periodo en que la vulnerabilidad permanece activa.
Resultado esperado: Reducción del 70-77% en MTTR, pasando a <=14 días. Meta:
80% de vulnerabilidades críticas/altas remediadas dentro del mismo sprint de 2 semanas
mediante reportes pedagógicos con código de ejemplo en Flutter/Dart que reducen
tiempo de compresión a menos de 2 horas.
5. Disminución de Falsos Positivos y Mejora de Eficiencia
Situación actual: Herramientas tradicionales de SAST presentan 30-40% de falsos
positivos, obligando a invertir 40-60 horas por sprint en validación manual, generando
fatiga de alertas y desconfianza.
Resultado esperado: Reducción del 50-62% en falsos positivos mediante correlación
inteligente SAST-DAST, pasando del 30-40% al menos del 15%. Ahorro de 25-40 horas
por sprint (325-520 horas anuales) redirigibles a desarrollo de funcionalidades de
negocio.
6. Mejora de Cumplimiento Normativo y Reducción de Riesgo Regulatorio
26
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Situación actual: Startups sin validación sistemática enfrentan riesgo de sanciones de
hasta 10% de ingresos anuales por incumplimiento de Decreto Legislativo N° 1531 y
normativas SBS/UIF-Perú.
Resultado esperado: Validación del 100% de controles OWASP MASVS L1
(esenciales) automáticamente. Reducción del 60-80% en hallazgos de auditorías
regulatorias. Reducción del tiempo de preparación para auditoría de 4-6 semanas a 3-5
días mediante reportes históricos de cumplimiento trazables.
7. Prevención de Incidentes y Retención de Usuarios
Situación actual: El 43% de usuarios abandona completamente una institución
financiera tras una brecha de seguridad (Neontri, 2025). Con CAC de USD 50-150 por
usuario y LTV de USD 500-1 500 (3-5 años), las pérdidas son significativas.
Resultado esperado: Reducción del 70-85% en incidentes de seguridad mediante
detección preventiva temprana. Prevención de abandono equivalente a USD 500-1 500
por usuario retenido. Ahorro de USD 200 000-500 000 por incidente mayor evitado
(costos de investigación forense, notificación, remediación y multas). La prevención de
un incidente que afecte 10 000 usuarios representa ahorro de USD 500 000-1 500 000.
8. Facilitación de Escalamiento y Acceso a Inversión
Situación actual: La ausencia de validación sistemática de seguridad es considerada red
flag por inversionistas institucionales (Acción Venture Lab, Quona Capital, ALLVP),
resultando en rechazo de inversión o valuación reducida en 15-30%.
Resultado esperado: Reducción del tiempo de due diligence técnico de 4-6 semanas a 1-
2 semanas mediante reportes históricos disponibles en menos de 24 horas. Eliminación
de red flags de seguridad que impactan valuación. Capacidad de responder a
cuestionarios de seguridad de clientes enterprisem facilitando a mercados que requieren
certificación de proveedores.
7 REFERENCIAS BIBLIOGRÁFICAS
20+ Application Security Statistics & Trends. (s/f). Recuperado el 12 de octubre de 2025, de
https://aimultiple.com/application-security-statistics
35 Phone Hacking and Mobile Security Stats | Certo Software. (s/f). Recuperado el 12 de octubre de
2025, de https://www.certosoftware.com/insights/phone-hacking-and-mobile-security-stats/
27
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
2024 Mobile App Security Statistics - Build38. (s/f). Recuperado el 12 de octubre de 2025, de
https://build38.com/blog/cybersecurity/2024-mobile-app-security-statistics/
2024 Q2 Mobile Landscape Threat Report. (s/f). Recuperado el 12 de octubre de 2025, de
https://www.lookout.com/threat-intelligence/report/q2-2024-mobile-landscape-threat-report
Best practices for enhancing security in fintech apps - Speednet. (s/f). Recuperado el 12 de octubre
de 2025, de https://speednetsoftware.com/best-practices-for-enhancing-security-in-fintech-
apps
Dawood, M., Tu, S., Xiao, C., Haris, M., Alasmary, H., Waqas, M., & Rehman, S. U. (2024). The
Impact of Domain Name Server (DNS) over Hypertext Transfer Protocol Secure (HTTPS) on
Cyber Security: Limitations, Challenges, and Detection Techniques. Computers, Materials and
Continua, 80(3), 4513–4542. https://doi.org/10.32604/CMC.2024.050049
Duy, P. N., & Cam, N. T. (2025). uitObfAMC: Obfuscated Android malware classification using deep
learning on multi-feature information approach. Information Sciences, 720, 122528.
https://doi.org/10.1016/J.INS.2025.122528
Ebbers, S., Gense, S., Bakkouch, M., Freiling, F., & Schinzel, S. (2024). Grand theft API: A forensic
analysis of vehicle cloud data. Forensic Science International: Digital Investigation, 48,
301691. https://doi.org/10.1016/J.FSIDI.2023.301691
Eichhorn, M., & Pugliese, G. (2024). Do You “Relay” Want to Give Me Away? – Forensic Cues of
Smart Relays and Their IoT Companion Apps. Forensic Science International: Digital
Investigation, 50, 301810. https://doi.org/10.1016/J.FSIDI.2024.301810
Empresas fintech en Perú: Oportunidades y retos para 2024. (s/f). Recuperado el 12 de octubre de
2025, de https://www.rextie.com/blog/oportunidades-de-las-fintech-en-peru/
Fintech Security Challenges and Protecting Financial Data| Quokka. (s/f). Recuperado el 12 de
octubre de 2025, de https://www.quokka.io/blog/fintech-security-challenges
Guía de Negocios FinTech 2024/2025 | EY - Perú. (s/f). Recuperado el 12 de octubre de 2025, de
https://www.ey.com/es_pe/insights/law/guia-fintech
Josephine, H. J. V. L., Rajagopal, M., Gayatri, S., & Lakshmi, K. (2025). Enhancing Mobile
Application Security Through Android Threat Classification. Procedia Computer Science, 252,
154–164. https://doi.org/10.1016/J.PROCS.2024.12.017
Latin America 2025 Mid-Year Cyber Snapshot Reveals 39% Surge in Attacks as AI Threats Escalate
Regional Risk Highlights from Latin America 2025 Cyber Threat Report - Check Point Blog.
(s/f). Recuperado el 12 de octubre de 2025, de https://blog.checkpoint.com/research/latin-
america-2025-mid-year-cyber-snapshot-reveals-39-surge-in-attacks-as-ai-threats-escalate-
regional-risk/
Madhushanie, N., Vidanagamachchi, S., & Arachchilage, N. (2025). Real-time privacy vulnerability
detection techniques in software development: A Systematic Literature Review. Computers &
Security, 159, 104659. https://doi.org/10.1016/J.COSE.2025.104659
Onik, A. R., Spinosa, T. T., Asad, A. M., & Baggili, I. (2024). Hit and run: Forensic vehicle event
reconstruction through driver-based cloud data from Progressive’s snapshot application.
Forensic Science International: Digital Investigation, 49, 301762.
https://doi.org/10.1016/J.FSIDI.2024.301762
Palutla, D. V., Bojjagani, S., Mula, S. C. R., Uyyala, R., Sharma, N. K., Morampudi, M. K., & Khan,
M. K. (2025). Unveiling Android security testing: A Comprehensive overview of techniques,
challenges, and mitigation strategies. Computers and Electrical Engineering, 127, 110620.
https://doi.org/10.1016/J.COMPELECENG.2025.110620
28
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Perú avanza en la regulación de las “fintech”: se aprobó el Reglamento de Modelos Novedosos de
la SBS | Garrigues. (s/f). Recuperado el 12 de octubre de 2025, de
https://www.garrigues.com/es_ES/noticia/peru-avanza-regulacion-fintech-aprobo-reglamento-
modelos-novedosos-sbs
Peru emerges as a land of opportunity for over 150 foreign Fintech startups - Finnosummit. (s/f).
Recuperado el 12 de octubre de 2025, de https://www.finnosummit.com/en/radar/peru-
emerges-as-a-land-of-opportunity-for-over-150-foreign-fintech-startups/
Perú registró 45 mil millones de ciberataques en 2024: así puedes proteger tu pyme sin ser experto
en tecnología - Infobae. (s/f). Recuperado el 12 de octubre de 2025, de
https://www.infobae.com/peru/2025/05/22/peru-registro-45-mil-millones-de-ciberataques-en-
2024-asi-puedes-proteger-tu-pyme-sin-ser-experto-en-tecnologia/
R. Arikkat, D., Vinod, P., Rehiman K.A., R., Nicolazzo, S., Arazzi, M., Nocera, A., & Conti, M.
(2025). DroidTTP: Mapping android applications with TTP for Cyber Threat Intelligence.
Journal of Information Security and Applications, 93, 104162.
https://doi.org/10.1016/J.JISA.2025.104162
Regulación Fintech Perú: 5 Claves de Supervisión | Guía 2024. (s/f). Recuperado el 12 de octubre
de 2025, de https://blog.acomo.pe/regulacion-fintech-peru/
Release v2.1.0 · OWASP/masvs. (s/f). Recuperado el 12 de octubre de 2025, de
https://github.com/OWASP/masvs/releases/tag/v2.1.0
Reporte del Sistema Nacional de Pagos y del sector Fintech en Perú - Marzo 2025. (s/f). Recuperado
el 12 de octubre de 2025, de https://www.bcrp.gob.pe/docs/Publicaciones/reporte-del-sistema-
nacional-de-pagos/2025/marzo/rspf-marzo-2025.html
Romdhana, A., Merlo, A., Ceccato, M., & Tonella, P. (2023). Assessing the security of inter-app
communications in android through reinforcement learning. Computers & Security, 131,
103311. https://doi.org/10.1016/J.COSE.2023.103311
Security Issues in Financial Technology Mobile Applications. (s/f). Recuperado el 12 de octubre de
2025, de https://approov.io/blog/vulnerabilities-in-fintech-mobile-apps
Senanayake, J., Kalutarage, H., Petrovski, A., Piras, L., & Al-Kadri, M. O. (2024). Defendroid: Real-
time Android code vulnerability detection via blockchain federated neural network with XAI.
Journal of Information Security and Applications, 82, 103741.
https://doi.org/10.1016/J.JISA.2024.103741
Shi, G., Li, T., Zhou, Q., Liu, M., & Feng, Y. (2025). Multi-dimensional assessment for Android
application security based on users’ evaluation. Computers & Security, 156, 104499.
https://doi.org/10.1016/J.COSE.2025.104499
Smmarwar, S. K., Gupta, G. P., & Kumar, S. (2024). Android malware detection and identification
frameworks by leveraging the machine and deep learning techniques: A comprehensive review.
Telematics and Informatics Reports, 14, 100130.
https://doi.org/10.1016/J.TELER.2024.100130
Taheri, R., Shojafar, M., Arabikhan, F., & Gegov, A. (2024). Unveiling vulnerabilities in deep
learning-based malware detection: Differential privacy driven adversarial attacks. Computers
& Security, 146, 104035. https://doi.org/10.1016/J.COSE.2024.104035
Top 10 Cybersecurity threats facing FinTech in 2024 - FinTech Strategy. (s/f). Recuperado el 12 de
octubre de 2025, de https://www.fintechstrategy.com/blog/2024/07/17/top-10-cybersecurity-
threats-facing-fintech-in-2024/
29
SEMINARIO DE INVESTIGACIÓN ACADÉMICA II 2025-01
Top 10 FinTech Cybersecurity Risks and Challenges in 2024 | SecOps® Solution. (s/f). Recuperado
el 12 de octubre de 2025, de https://www.secopsolution.com/blog/top-10-fintech-
cybersecurity-risks-and-challenges
Top Fintech Security Threats and How to Mitigate Them. (s/f). Recuperado el 12 de octubre de 2025,
de https://neontri.com/blog/fintech-security/
Xiang, D., Lin, S., Huang, K., Ding, Z., Liu, G., & Li, X. (2025). A fine-grained approach for Android
taint analysis based on labeled taint value graphs. Computers & Security, 148, 104162.
https://doi.org/10.1016/J.COSE.2024.104162
Zhang, D., Yang, X., Liu, S., Zhou, Y., Fu, J., & Peng, G. (2025). A survey on Android dynamic
evasive malware: Taxonomy, countermeasures and open challenges. Computers &
Security, 159, 104646. https://doi.org/10.1016/J.COSE.2025.104646
