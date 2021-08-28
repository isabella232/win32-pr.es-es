---
title: Kit de herramientas de evaluación de Windows
description: Kit de herramientas de evaluación de Windows
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6eff172a59a7f0ee00f85a0cd8f237387aaa78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482681"
---
# <a name="windows-assessment-toolkit"></a>Kit de herramientas de evaluación de Windows

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 7 \| Windows 8  

## <a name="description"></a>Descripción

El Windows Assessment Toolkit y Windows Performance Toolkit que Windows Assessment and Deployment Kit (ADK). Juntos proporcionan una solución completa para evaluar el rendimiento general del equipo y automatizar la implementación del Windows operativo en equipos nuevos.

Este tema se centra en **la** Toolkit . Los resultados de la evaluación se usan para diagnosticar posibles problemas, de modo que el hardware y el software que desarrolle respondan y tengan un impacto mínimo en la duración de la batería, el rendimiento de inicio y el tiempo de apagado. Las mismas evaluaciones están disponibles para asociados OEM, asociados de ISV/IHV, seguidores y otros miembros de la comunidad, para establecer un marco común para medir, comparar y revisar aspectos de calidad.

Mediante el uso de Windows de evaluación, puede medir distintos aspectos del rendimiento en una variedad de escenarios, desde el tiempo de arranque hasta el rendimiento de la duración de la batería hasta el streaming de vídeo de alta definición. Las evaluaciones pueden identificar posibles problemas, un comportamiento incoherente y resaltar las áreas que se deben investigar.

En versiones anteriores de Windows, había varias herramientas disponibles para medir la calidad, como Velocity Test Suite (VTS/UNO), Fundamental Quality Tools Suite (FQTS) y System Power and Performance Tools Suite (SPPTS). Assessment Toolkit combina la funcionalidad de estas herramientas de diagnóstico de rendimiento en un conjunto integrado de herramientas que es más fácil de usar y proporciona resultados más amplios y significativos.

El Windows assessment Toolkit maximiza la satisfacción del consumidor al:

-   Le ayuda a evaluar la experiencia general de Windows software, controladores y controladores de valor agregado, y configuraciones de hardware
-   Proporcionar datos detallados del sistema que pueden ayudarle a identificar las causas principales de los problemas de calidad
-   Reducir los costos mediante la revelación de problemas durante el desarrollo
-   Generación de comparaciones de resultados de equipos diferentes o del mismo conjunto de equipos a lo largo del tiempo mediante la creación de gráficos de comparación a partir de varios conjuntos de resultados
-   Generación de comentarios en un formato estandarizado que puede usar para mejorar la calidad de los productos

Se pueden lograr objetivos empresariales importantes mediante el uso de las evaluaciones Toolkit:

-   **Medición &** comparación: puede usar los datos para comparar componentes (software, controladores o ambos) con otros componentes similares para facilitar la toma de decisiones, las recomendaciones y el distintivo de banco competitivo.
-   **Mejorar la** calidad: puede trabajar de forma independiente o con asociados implicados para crear un componente (software, controlador o ambos) según los criterios de calidad predefinidos.
-   **Seguimiento de la calidad**   Puede crear un proceso para realizar un seguimiento eficaz de la calidad de las versiones de los componentes y detectar regresiones después de cada iteración.

## <a name="usage-and-best-practices"></a>Uso y procedimientos recomendados

Las evaluaciones son una combinación de archivos XML y binarios que inducen un conjunto específico de estados en un equipo, miden y registran la actividad y conservan los resultados registrados. Un trabajo es una colección de una o varias evaluaciones y su configuración, que se ejecutan a la vez en un equipo. La plataforma de evaluación proporciona la infraestructura para ejecutar y mostrar trabajos, evaluaciones y resultados de forma coherente. Los resultados suelen incluir información de diagnóstico e corrección que le ayuda a determinar las áreas que necesitan una investigación adicional y una acción correctiva. Puede:

-   Ejecutar evaluaciones en un solo equipo o en una pequeña colección de equipos con **Windows Assessment Console** (Windows AC) <dl> Este escenario es para los usuarios que desean ver las características de rendimiento en una o varias configuraciones de equipo diferentes. Windows AC es una interfaz gráfica de usuario (GUI) que se usa para agrupar las evaluaciones, crear un trabajo, empaquetar un trabajo, ejecutar el trabajo y administrar los resultados del trabajo. Los resultados suelen incluir acciones recomendadas.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Este escenario es principalmente para los usuarios que desean ejecutar un conjunto de evaluaciones cualitativas en una línea completa de equipos de escritorio, portátiles o tabletas en un entorno de desarrollo.  
    </dl>

La página Toolkit evaluación ofrece estas características:

-   Una interfaz gráfica de usuario (GUI) sencilla y evaluaciones que se pueden usar para evaluar un equipo sin conocimientos técnicos exhaustivos del sistema
-   Resultados de la evaluación, que se ven en la consola o la interfaz de usuario, que a menudo incluyen recomendaciones para ayudarle a mejorar el sistema.
-   La capacidad de ejecutar un trabajo preconfigurado con un solo clic
-   Configuración de evaluación predefinida en cada evaluación de trabajo preconfigurada para que pueda ejecutar un trabajo en varios equipos y estar seguro de que los resultados son comparables
-   Trabajos que se pueden personalizar para incluir las evaluaciones que desea usar y la configuración que desea usar.
-   Sintaxis de línea de comandos de Assessment Platform para scripting y automatización de trabajos
-   La capacidad de ejecutar un trabajo, ver los resultados, realizar pasos de corrección para mejorar el sistema y, a continuación, volver a ejecutar el trabajo y comparar los nuevos resultados en paralelo con los resultados anteriores para ver cómo ha mejorado el sistema

La evaluación Toolkit suele usarse en estos escenarios:




| Escenario | Descripción | 
|----------|-------------|
| "Caja negra" | Ejecute un trabajo predefinido y examine los resultados en busca de valores inusuales o indicaciones de problemas con los controladores, el uso de memoria u otras áreas que abordan las evaluaciones. | 
| Comparación de resultados | <ol><li>Ejecute una evaluación única con la configuración recomendada en cualquier equipo que ejecute un sistema operativo compatible.</li><li>Use la Windows ac para empaquetar el trabajo para que se ejecute en otro equipo.</li><li>Guarde los resultados en un recurso compartido para poder comparar los resultados.</li><li>Compare los resultados de cualquier Windows equipo con los de cualquier otro sistema operativo compatible para identificar las diferencias.</li></ol><br /> | 
| Limpiar equipo | Ejecute evaluaciones en un equipo limpio que incluya solo el sistema operativo para establecer los resultados del sistema de línea de base. | 
| Equipo con componentes de hardware o software agregados | Agregue nuevo hardware o software al sistema de equipo limpio y, a continuación, vuelva a ejecutar las evaluaciones para comparar los resultados con resultados limpios del equipo. | 
| Creación de evaluaciones | Use API públicas para desarrollar o ampliar una evaluación, o integrar evaluaciones con sus herramientas e infraestructura. | 




 

Estas evaluaciones se pueden usar:



| Evaluación                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Validación previa de la certificación de controladores          | La **evaluación de la validación** previa de la certificación de controladores comprueba que los controladores de un sistema Windows operativo en ejecución son aptos para el Windows de certificación. Los resultados incluyen recomendaciones que le ayudarán a resolver problemas que encuentra la evaluación, como controladores sin firmar o firmas expiradas.                                                                                                                                                                                                                                                            |
| Comprobación del controlador                          | La **evaluación comprobación del** controlador comprueba que una imagen de Windows sin conexión o un sistema operativo Windows en ejecución contiene el conjunto correcto de controladores. Los resultados incluyen recomendaciones para ayudarle a resolver cualquier problema que encuentre la evaluación. Estos problemas pueden incluir controladores que faltan, duplicados, antiguos o innecesarios.                                                                                                                                                                                                                                         |
| Control de archivos                                | La **evaluación de control de** archivos proporciona una manera automatizada de realizar operaciones comunes de archivos y capturar métricas. Las métricas miden las duraciones y el rendimiento para ayudarle a comprender el rendimiento de un equipo en escenarios de control de archivos del usuario final. La evaluación del control de archivos usa un conjunto de cargas de trabajo para simular un usuario que copia, mueve, comprime, descomprime y elimina archivos y carpetas en sistemas cliente.                                                                                                                                       |
| Tratamiento de fotos                               | La **evaluación de tratamiento** de fotos mide el rendimiento del equipo y la duración de la batería mediante la simulación de un usuario final que está viendo y manipulando fotos.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Internet Explorer iniciar o crear pestañas          | La **Internet Explorer de rendimiento de inicio** ayuda a identificar los componentes que pueden afectar al tiempo necesario para iniciar Internet Explorer. La evaluación mide el tiempo para representar completamente una página en blanco, incluido el tiempo de carga del proceso de IExplore.exe y los intervalos de creación de fotogramas y creación de tabulaciones. También mide el efecto de todas las extensiones, complementos y barras de herramientas que están instaladas en el sistema. No mide el rendimiento de la red ni de exploración.                                                                                         |
| Activado/Desactivado                                       | La **evaluación de transición de** encendido/apagado mide el rendimiento de Windows 8 escenarios de rendimiento de arranque, espera e hibernación.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Internet Explorer rendimiento de exploración       | La **Internet Explorer rendimiento de** exploración mide la calidad de la experiencia de exploración en Internet Explorer y evalúa las funcionalidades de hardware gráfico y CPU. Se proporcionan tres cargas de trabajo de exploración independientes para hacer que el equipo se estrese de varias maneras.                                                                                                                                                                                                                                                                                                  |
| Rendimiento de transcodificación multimedia                | La **evaluación transcodificación de** vídeo mide el proceso de cambiar un archivo de vídeo a un formato o velocidad de bits diferente. Esta evaluación ejecuta una serie de operaciones de transcodificación con formatos y resoluciones comunes de archivos de entrada y salida                                                                                                                                                                                                                                                                                                                                           |
| Windows Rendimiento de la interfaz de usuario                       | La **Windows de rendimiento de la interfaz de** usuario evalúa el rendimiento de algunas experiencias básicas dentro de Windows interfaz de usuario. La evaluación mide la capacidad de respuesta y la calidad de la representación mientras la evaluación hace ejercicios de cargas de trabajo que simulan actividades del usuario, como el uso de la búsqueda y la transición del entorno de aplicación de Windows Store al escritorio. Los resultados de la capacidad de respuesta se miden en milisegundos. Los números bajos significan que el equipo es más rápido y con mayor capacidad de respuesta. Para la representación, los resultados muestran la velocidad de fotogramas y el número de problemas que se producen. |
| Superficie de memoria                             | Puede usar la evaluación de **la superficie de** memoria para comparar cuantitativamente una imagen de sistema operativo de línea base con otra imagen de sistema operativo. A continuación, puede identificar los componentes específicos que afectan a la superficie de memoria del sistema físico. Estos componentes pueden incluir controladores, aplicaciones de complementos, paquetes de software cargados previamente y programas antivirus.                                                                                                                                                                                                           |
| Rendimiento del primer arranque                       | La **evaluación del rendimiento del** primer arranque identifica los problemas que afectan al tiempo Windows que se tarda en arrancar y muestra el pantalla Inicio la primera vez que se inicia el equipo. Los resultados ayudan a los OEM a diagnosticar qué provoca retrasos y proporcionan recomendaciones para mejorar la experiencia.                                                                                                                                                                                                                                                                                      |
| Streaming multimedia                              | La **evaluación del rendimiento de streaming** multimedia le ayuda a evaluar el rendimiento de la configuración de un equipo al transmitir elementos multimedia mediante Internet Explorer. Puede usar los resultados de la evaluación para comprender, comparar y mejorar la experiencia de streaming multimedia.                                                                                                                                                                                                                                                                                                                 |
| WinSAT completo                         | La **Windows System Assessment (WinSAT)** se usa para evaluar y mejorar el rendimiento de un equipo en varios componentes del sistema, como CPU, memoria, disco y gráficos. Los resultados de la evaluación completa de WinSAT expresan la funcionalidad de la configuración de hardware de un equipo en números. Las puntuaciones más altas suelen significar que el equipo evaluado funciona mejor y más rápido que un equipo con una puntuación inferior.                                                                                                                                                        |
| Eficiencia energética                            | El **trabajo eficiencia energética** proporciona una manera automatizada de evaluar la duración de la batería de un equipo. Con las cargas de trabajo, el trabajo de eficiencia energética también realiza diagnósticos que evalúan si los componentes del sistema usan energía cuando deben estar inactivos.                                                                                                                                                                                                                                                                                                               |
| Diagnóstico de minifiltro Configuración               | La **opción De diagnóstico de MiniFiltro** se ejecuta dentro de Internet Explorer de rendimiento de inicio, la evaluación de control de archivos y la evaluación del rendimiento de arranque (Windows 8). Si selecciona esta opción en las evaluaciones que ofrecen la opción de diagnóstico MiniFilter, se generan métricas que le ayudarán a evaluar el impacto de las operaciones de MiniFilter en varios escenarios de evaluación.                                                                                                                                                                                  |
| Reproductor de Windows Media Rendimiento y calidad | La **Reproductor de Windows Media rendimiento** y calidad inicia WMP y reproduce varios clips multimedia uno tras otro para capturar métricas de rendimiento y calidad relacionadas con la reproducción multimedia.                                                                                                                                                                                                                                                                                                                                                                          |



 

Otras herramientas, como el Windows rendimiento Toolkit, se incluyen en el ADK. Estas herramientas proporcionan información detallada que le permite analizar y realizar un seguimiento del rendimiento del sistema y de la aplicación. Consulte la sección Recursos a continuación para obtener más información.

## <a name="resources"></a>Recursos

**Video:**

-   [Vídeos de ADK de Channel9 BUILD](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Documentación:**

-   [Windows Assessment and Deployment Kit](/previous-versions/windows/hh825420(v=win.10))
-   [Windows Referencia técnica Toolkit evaluación](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Motor de ejecución de evaluaciones](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Windows Análisis de rendimiento](https://msdn.microsoft.com/performance/default.aspx)

  


 

