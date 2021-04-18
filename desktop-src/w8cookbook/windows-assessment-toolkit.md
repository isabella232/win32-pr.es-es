---
title: Kit de herramientas de evaluación de Windows
description: Kit de herramientas de evaluación de Windows
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d75aa02757acb54083e005d67a10e0fa42efec
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "105705071"
---
# <a name="windows-assessment-toolkit"></a>Kit de herramientas de evaluación de Windows

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 7 \| Windows 8  

## <a name="description"></a>Descripción

El kit de herramientas de evaluación de Windows y el kit de herramientas de rendimiento de Windows componen Windows Assessment and Deployment Kit (ADK). Juntos proporcionan una solución completa para evaluar el rendimiento general del equipo y automatizar la implementación del sistema operativo Windows en equipos nuevos.

Este tema se centra en el **Kit de herramientas de evaluación**. Los resultados de la evaluación se usan para diagnosticar posibles problemas, de modo que el hardware y el software que desarrolle tengan capacidad de respuesta y tenga un impacto mínimo en la duración de la batería, el rendimiento de inicio y el tiempo de apagado. Las mismas evaluaciones están disponibles para asociados de OEM, asociados de ISV/IHV, entusiastas y otros miembros de la comunidad, a fin de establecer un marco común para medir, comparar y revisar aspectos de calidad.

Con las herramientas de evaluación de Windows, puede medir distintos aspectos del rendimiento en diversos escenarios, desde el tiempo de arranque hasta el rendimiento de la batería hasta el streaming de vídeo de alta definición. Las evaluaciones pueden identificar posibles problemas, un comportamiento incoherente y resaltar las áreas que se deben investigar.

En las versiones anteriores de Windows, había varias herramientas disponibles para medir la calidad, incluido el conjunto de pruebas de progreso (VTS/VOS), el conjunto de herramientas de calidad fundamental (FQTS) y el conjunto de herramientas de energía y rendimiento (SPPTS) del sistema. El kit de herramientas de evaluación combina la funcionalidad de estas herramientas de diagnóstico de rendimiento en un conjunto integrado de herramientas que es más fácil de usar y proporciona resultados más amplios y significativos.

El kit de herramientas de evaluación de Windows maximiza la satisfacción del consumidor mediante:

-   Ayudarle a evaluar la experiencia global de Windows, el software y los controladores de valor añadido y las configuraciones de hardware.
-   Proporcionar datos de sistema detallados que pueden ayudarle a identificar las causas raíz de los problemas de calidad
-   Reducción de los costos al revelar problemas durante el desarrollo
-   Generar comparaciones de los resultados de distintos equipos o del mismo conjunto de equipos con el tiempo creando gráficos de comparación a partir de varios conjuntos de resultados
-   Generación de comentarios en un formato estandarizado que se puede usar para mejorar la calidad de los productos

Se pueden lograr objetivos empresariales importantes mediante el uso del kit de herramientas de evaluaciones:

-   **Medida & comparación** : puede usar los datos para comparar componentes (software, controladores o ambos) con otros componentes similares para facilitar la toma de decisiones, las recomendaciones y el marcado de bancos competitivos.
-   **Mejorar la calidad** : puede trabajar de forma independiente o con asociados para compilar un componente (software, controlador o ambos) según los criterios de calidad predefinidos.
-   **Calidad de seguimiento**   Puede crear un proceso para realizar un seguimiento eficaz de la calidad de las versiones de los componentes y detectar las regresiones después de cada iteración.

## <a name="usage-and-best-practices"></a>Uso y procedimientos recomendados

Las evaluaciones son una combinación de archivos XML y binarios que inducen un conjunto específico de Estados en un equipo, miden y registran la actividad y conservan los resultados registrados. Un trabajo es una colección de una o más evaluaciones y su configuración, que se ejecutan al mismo tiempo en un equipo. La plataforma de evaluación proporciona la infraestructura para la ejecución coherente y la visualización de trabajos, evaluaciones y resultados. Los resultados suelen incluir información de diagnóstico y corrección que le ayuda a determinar las áreas que necesitan investigación adicional y medidas correctivas. Puede:

-   Ejecutar evaluaciones en un solo equipo o en una pequeña colección de equipos con la **consola de evaluación de Windows** (Windows AC) <dl> Este escenario se refiere a los usuarios que quieren ver las características de rendimiento en una o varias configuraciones de equipo diferentes. Windows AC es una interfaz gráfica de usuario (GUI) que se usa para agrupar las evaluaciones, crear un trabajo, empaquetar un trabajo, ejecutar el trabajo y administrar los resultados del trabajo. Los resultados suelen incluir las acciones recomendadas.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Este escenario es principalmente para los usuarios que quieren ejecutar un conjunto de evaluaciones cualitativas en una línea completa de equipos de escritorio, portátiles o Tablet PC en un entorno de desarrollo.  
    </dl>

El kit de herramientas de evaluación ofrece estas características:

-   Una interfaz gráfica de usuario (GUI) sencilla y valoraciones que se pueden usar para evaluar un equipo sin tener conocimientos técnicos detallados del sistema.
-   Resultados de la evaluación, que se ven en la consola o en la interfaz de usuario, que suelen incluir recomendaciones para ayudarle a mejorar el sistema
-   La capacidad de ejecutar un trabajo preconfigurado con un solo clic
-   Configuración de evaluación predefinida en cada evaluación de trabajo preconfigurada para que pueda ejecutar un trabajo en varios equipos y estar seguro de que los resultados son comparables
-   Trabajos que se pueden personalizar para incluir las evaluaciones que quiere usar y la configuración que desea usar
-   Sintaxis de línea de comandos de la plataforma de evaluación para scripting y automatización de trabajos
-   La capacidad de ejecutar un trabajo, ver los resultados, tomar medidas de corrección para mejorar el sistema y, a continuación, volver a ejecutar el trabajo y comparar los nuevos resultados en paralelo con los resultados anteriores para ver el modo en que el sistema ha mejorado.

El kit de herramientas de evaluación se usa normalmente en estos escenarios:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Escenario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Cuadro negro&quot;</td>
<td>Ejecutar un trabajo predefinido y examinar los resultados para comprobar si hay valores inusuales o indicaciones de problemas con los controladores, el uso de memoria u otras áreas que resuelven las evaluaciones.</td>
</tr>
<tr class="even">
<td>Comparar resultados</td>
<td><ol>
<li>Ejecute una sola evaluación con la configuración recomendada en cualquier equipo que ejecute un sistema operativo compatible.</li>
<li>Use la AC de Windows para empaquetar el trabajo para que se ejecute en otro equipo.</li>
<li>Guarde los resultados en un recurso compartido para poder comparar los resultados.</li>
<li>Compare los resultados de cualquier equipo de Windows con los de cualquier otro sistema operativo compatible para identificar las diferencias.</li>
</ol>
<br/></td>
</tr>
<tr class="odd">
<td>Limpiar equipo</td>
<td>Ejecute evaluaciones en un equipo limpio que solo incluya el sistema operativo para establecer resultados del sistema de línea base.</td>
</tr>
<tr class="even">
<td>Equipo con componentes de hardware o software agregados</td>
<td>Agregue nuevo hardware o software al equipo limpio y, a continuación, vuelva a ejecutar las evaluaciones para comparar los resultados con los resultados del equipo limpio.</td>
</tr>
<tr class="odd">
<td>Crear evaluaciones</td>
<td>Use API públicas para desarrollar o ampliar una evaluación, o bien integre evaluaciones con sus herramientas e infraestructura.</td>
</tr>
</tbody>
</table>



 

Estas evaluaciones se pueden usar:



| Evaluación                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Validación previa de la certificación del controlador          | La evaluación de la **validación previa de la certificación del controlador** comprueba que los controladores de un sistema operativo Windows en ejecución cumplen con el programa de certificación de Windows. Los resultados incluyen recomendaciones que le ayudarán a resolver los problemas que encuentra la evaluación, como controladores sin firmar o firmas expiradas.                                                                                                                                                                                                                                                            |
| Comprobación del controlador                          | La evaluación de **comprobación de controladores** comprueba que una imagen de Windows sin conexión o un sistema operativo Windows en ejecución contiene el conjunto de controladores correcto. Los resultados incluyen recomendaciones para ayudarle a resolver cualquier problema que encuentre la evaluación. Estos problemas pueden incluir controladores ausentes, duplicados, antiguos o innecesarios.                                                                                                                                                                                                                                         |
| Control de archivos                                | La evaluación de **control de archivos** proporciona una forma automatizada de realizar operaciones comunes de archivos y capturar métricas. Las métricas miden la duración y el rendimiento para ayudarle a entender cómo funciona un equipo en los escenarios de control de archivos de usuario final. La evaluación de control de archivos utiliza un conjunto de cargas de trabajo para simular a un usuario que está copiando, moviendo, comprimiendo, descomprimiendo y eliminando archivos y carpetas en los sistemas cliente.                                                                                                                                       |
| Control de fotografías                               | La evaluación de **control de fotografías** mide el rendimiento del equipo y la duración de la batería mediante la simulación de un usuario final que está viendo y manipulando fotografías.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Inicio o pestaña creación de Internet Explorer          | La evaluación del **rendimiento de inicio de Internet Explorer** ayuda a identificar los componentes que pueden afectar al tiempo necesario para iniciar Internet Explorer. La evaluación mide el tiempo para representar por completo una página en blanco, incluido el tiempo de carga del proceso de IExplore.exe y los intervalos de creación de Marcos y creación de pestañas. También mide el efecto de todas las extensiones, complementos y barras de herramientas que están instalados en el sistema. No mide ningún rendimiento de la red ni de la exploración.                                                                                         |
| Activado/Desactivado                                       | La evaluación **de transición ON/OFF** mide el rendimiento de los escenarios de rendimiento de arranque, espera e hibernación de Windows 8.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Rendimiento de exploración de Internet Explorer       | La evaluación de **rendimiento de exploración de Internet Explorer** mide la calidad de la experiencia de exploración en Internet Explorer y evalúa las capacidades de hardware de gráficos y CPU. Se proporcionan tres cargas de trabajo de exploración independientes para recargar el equipo de varias maneras.                                                                                                                                                                                                                                                                                                  |
| Rendimiento de transcodificación de elementos multimedia                | La evaluación de **transcodificación de vídeo** mide el proceso de cambio de un archivo de vídeo a un formato o velocidad de bits diferente. Esta evaluación ejecuta una serie de operaciones de transcodificación con formatos y resoluciones de archivos de entrada y salida comunes.                                                                                                                                                                                                                                                                                                                                           |
| Rendimiento de la interfaz de usuario de Windows                       | La evaluación de **rendimiento de Windows UI** evalúa el rendimiento de algunas experiencias básicas dentro de la interfaz de usuario de Windows. La evaluación mide la calidad de la capacidad de respuesta y la representación mientras la evaluación ejercita las cargas de trabajo que simulan las actividades de usuario, como el uso de la búsqueda y la transición desde el entorno de aplicaciones de la tienda Windows al escritorio. Los resultados de la capacidad de respuesta se miden en milisegundos. Los números bajos significan que el equipo es más rápido y con mayor capacidad de respuesta. Para la representación, los resultados muestran la velocidad de fotogramas y el número de problemas que se producen. |
| Superficie de memoria                             | Puede usar la evaluación de **superficie de memoria** para comparar cuantitativamente una imagen de sistema operativo de línea base con otra imagen de sistema operativo. A continuación, puede identificar los componentes específicos que afectan a la superficie de memoria del sistema físico. Estos componentes pueden incluir controladores, aplicaciones de complementos, paquetes de software cargados previamente y programas antivirus.                                                                                                                                                                                                           |
| Rendimiento del primer arranque                       | La **primera** evaluación del rendimiento de arranque identifica los problemas que afectan al tiempo que tarda Windows en arrancarse y muestran la pantalla Inicio la primera vez que se inicia el equipo. Los resultados ayudan a los OEM a diagnosticar lo que provoca retrasos y proporcionan recomendaciones para mejorar la experiencia.                                                                                                                                                                                                                                                                                      |
| Transmisión por secuencias de multimedia                              | La evaluación del rendimiento de los **medios de streaming** le ayuda a evaluar el rendimiento de la configuración de un equipo al transmitir contenido multimedia con Internet Explorer. Puede usar los resultados de la evaluación para comprender, comparar y mejorar la experiencia de streaming multimedia.                                                                                                                                                                                                                                                                                                                 |
| Completo de WinSAT                         | La **evaluación del sistema de Windows (WinSAT)** se usa para valorar y mejorar el rendimiento de un equipo en varios componentes del sistema, como la CPU, la memoria, el disco y los gráficos. Los resultados de la evaluación completa de WinSAT expresan la capacidad de una configuración de hardware de equipo en números. Las puntuaciones más altas suelen significar que el equipo evaluado funciona mejor y más rápido que un equipo con una puntuación inferior.                                                                                                                                                        |
| Eficiencia energética                            | El trabajo de **eficiencia energética** proporciona una forma automatizada de evaluar la duración de la batería de un equipo. Con las cargas de trabajo, el trabajo de eficiencia energética también realiza diagnósticos que evalúan si los componentes del sistema están usando energía cuando deben estar inactivos.                                                                                                                                                                                                                                                                                                               |
| Configuración de diagnóstico de minifiltro               | La opción de **diagnóstico de minifiltro** se ejecuta en la evaluación de rendimiento de inicio de Internet Explorer, en la evaluación de control de archivos y en la evaluación de rendimiento de arranque (Windows 8). La selección de esta opción en las evaluaciones que ofrecen la opción de diagnóstico de minifiltro genera métricas que le ayudan a evaluar el impacto de las operaciones de minifiltro en varios escenarios de evaluación.                                                                                                                                                                                  |
| Rendimiento y calidad de Windows Media Player | La evaluación de **rendimiento y calidad de Windows Media Player** inicia WMP y reproduce varios clips multimedia uno tras otro para capturar las métricas de rendimiento y calidad relacionadas con la reproducción multimedia.                                                                                                                                                                                                                                                                                                                                                                          |



 

Otras herramientas, como el kit de herramientas de rendimiento de Windows, se incluyen en el ADK. Estas herramientas proporcionan información detallada que le permite analizar y realizar un seguimiento del rendimiento del sistema y de las aplicaciones. Vea la sección recursos a continuación para obtener más información.

## <a name="resources"></a>Recursos

**Cámara**

-   [Vídeos de la compilación de Channel9](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Documentación**

-   [Windows Assessment and Deployment Kit](/previous-versions/windows/hh825420(v=win.10))
-   [Referencia técnica del kit de herramientas de evaluación de Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Motor de ejecución de evaluaciones](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Análisis de rendimiento de Windows](https://msdn.microsoft.com/performance/default.aspx)

  


 

