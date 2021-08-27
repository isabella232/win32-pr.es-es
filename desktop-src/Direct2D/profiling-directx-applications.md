---
title: Generación de perfiles de aplicaciones de DirectX
description: Muestra cómo medir algunas de las medidas de tiempo de rendimiento más importantes para una aplicación DirectX mediante las herramientas XPerf y GPUView que se envían como parte de la Windows rendimiento Toolkit.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c923f2917dbb8695bcd624f4d998043e7218cf2f976b19b24ab4cff2bc65f398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665468"
---
# <a name="profiling-directx-apps"></a>Generación de perfiles de aplicaciones de DirectX

Esto muestra cómo medir algunas de las medidas de tiempo de rendimiento más importantes para una aplicación [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) mediante las herramientas **XPerf** y **GPUView** que se envían como parte de la Windows Rendimiento Toolkit. Esta no es una guía completa para comprender las herramientas, sino su aplicabilidad específica para analizar el rendimiento de la aplicación DirectX. Aunque la mayoría de las técnicas que se analizan aquí son relevantes para todas las aplicaciones de DirectX, es más relevante para las aplicaciones que usan cadenas de intercambio y no para las aplicaciones DirectX creadas en XAML que usan animaciones SIS/VSIS y XAML. Le llevamos por las medidas clave del tiempo de rendimiento, cómo adquirir e instalar las herramientas, y realizar seguimientos de medición del rendimiento y, a continuación, analizarlas para comprender los cuellos de botella de la aplicación.

## <a name="about-the-tools"></a>Acerca de las herramientas

### <a name="xperf"></a>**XPerf**

**XPerf** es un conjunto de herramientas de análisis de rendimiento creadas sobre seguimiento de eventos para Windows (ETW) diseñadas para medir y analizar el rendimiento detallado del sistema y la aplicación y el uso de recursos. A partir Windows 8 esta herramienta de línea de comandos tiene una interfaz gráfica de usuario y se denomina Windows Performance Recorder (WPR) y Windows Analizador de rendimiento (WPA). Puede encontrar más información sobre estas herramientas en la página web de [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): Windows Performance [Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Un ETW recopila los eventos de kernel solicitados y los guarda en un archivo denominado archivo de registro de seguimiento de eventos (ETL). Estos eventos de kernel proporcionan información amplia sobre una aplicación y las características del sistema al ejecutar la aplicación. Los datos se recopilan habilitando la captura de seguimiento, realizando el escenario de aplicación deseado que necesita análisis, deteniendo la captura que guarda los datos en un archivo ETL. A continuación, puede analizar el archivo en el mismo equipo o en otro mediante la herramienta de línea de **comandosxperf.exe** o la herramienta de análisis de seguimiento visual **xperfview.exe**.

### <a name="gpuview"></a>GPUView

**GPUView es** una herramienta de desarrollo para determinar el rendimiento de la unidad de procesamiento gráfico (GPU) y la CPU. Examina el rendimiento con respecto al procesamiento del búfer de acceso directo a memoria (DMA) y el resto del procesamiento de vídeo en el hardware de vídeo.

En el caso de las aplicaciones de [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) que dependen en gran medida de la GPU, **GPUView** es una herramienta eficaz para comprender la relación entre el trabajo realizado en la CPU y la GPU. Para obtener más información sobre **GPUView,** [consulte Uso de GPUView.](/windows-hardware/drivers/display/using-gpuview)

De forma similar a **XPerf,** primero se realiza un seguimiento ETW iniciando el servicio de seguimiento, iniciando el escenario que necesita análisis para la aplicación en consideración, deteniendo el servicio y guardando la información en un archivo ETL. **GPUView** presenta los datos presentes en el archivo ETL en un formato gráfico.

Después de instalar **la herramienta GPUView,** se recomienda leer el tema "Pantalla principal de **GPUView"** en el menú "Ayuda **de GPUView".** Contiene información útil sobre cómo interpretar la interfaz **de usuario de GPUView.**

## <a name="installing-the-tools"></a>Instalación de las herramientas

**XPerf** y **GPUView se** incluyen en Windows Performance Toolkit (WPT).

**XPerf se** distribuye como parte del kit de desarrollo Windows software (SDK) para Windows. [Descargue el SDK Windows](https://dev.windows.com/downloads).

**GPUView** está disponible en Windows Assessment and Deployment Kit (Windows ADK). [Descargue el Windows ADK](/windows-hardware/get-started/adk-install).

Después de la instalación, debe agregar los directorios que contienen **XPerf** y **GPUView** a la variable "Path" del sistema.

Haga clic en botón Inicio y escriba "Variables del sistema". Se abre la ventana Propiedades sistema. Haga clic en "Editar las variables de entorno del sistema". Seleccione "Variables de entorno" en el cuadro de diálogo "Propiedades del sistema". La variable "Path" se encuentra en "Variables del sistema". Anexe el directorio que **contienexperf.exe** y **GPUView.exe** a la ruta de acceso. Estos archivos ejecutables se encuentran en el directorio "Windows Rendimiento Toolkit" dentro de "Windows Kits". La ubicación predeterminada es: C: Archivos de **\\ programa (x86) Windows \\ Kits \\ 10 \\ Windows Rendimiento Toolkit**.

## <a name="performance-time-measurements"></a>Medidas de tiempo de rendimiento

La mayoría de las aplicaciones esperan ejecutarse sin problemas y responder a la entrada del usuario. Sin embargo, en función del escenario que desee, un aspecto del rendimiento podría ser más importante que otro. Por ejemplo, para una aplicación de lector de noticias que se ejecuta en un equipo con tableta táctil, el aspecto más importante es ver un único artículo a la vez y desplazarse por el mismo artículo o por otro diferente. En este escenario, no es necesaria la capacidad de representar todo el contenido de cada fotograma. Sin embargo, la capacidad de desplazarse por el artículo sin problemas en un gesto táctil es muy importante.

En otra instancia, un juego o una aplicación de representación de vídeo que usa muchas animaciones tiene problemas si se descartan fotogramas. En este caso, la capacidad de presentar contenido en la pantalla sin interupción de la entrada del usuario es muy importante.

Para entender qué parte de la aplicación es problemática, el primer paso es decidir los escenarios más importantes. Una vez que se entienden los aspectos básicos de la aplicación y cómo se van a realizar, resulta más fácil buscar problemas con las herramientas.

Algunas de las métricas de tiempo de rendimiento más comunes son las siguientes:

### <a name="startup-time"></a>Tiempo de inicio

Tiempo medido desde el inicio del proceso hasta la primera vez que se alcanza la pantalla. Esta medida es más útil cuando el sistema está caliente, lo que significa que la medida se toma después de iniciar la aplicación varias veces.

### <a name="cpu-time-per-frame"></a>Tiempo de CPU por fotograma

Tiempo durante el cual la CPU procesa activamente la carga de trabajo de la aplicación para un fotograma. Si la aplicación se ejecuta sin problemas, todo el procesamiento necesario para un fotograma se produce dentro de un intervalo de sincronización de v. Con la frecuencia de actualización del monitor de 60Hz, esto llega a 16 ms por fotograma. Si el tiempo o el marco de CPU es superior a 16 ms, es posible que se necesiten optimizaciones de CPU para generar una experiencia de aplicación sin problemas.

### <a name="gpu-time-per-frame"></a>Tiempo de GPU por fotograma

Tiempo durante el cual GPU procesa activamente la carga de trabajo de la aplicación para un fotograma. Una aplicación está enlazada a GPU cuando el tiempo que se necesita para procesar un marco de datos es superior a 16 ms.

La capacidad de entender si una aplicación está enlazada a CPU o GPU restringirá la parte problemática del código.

## <a name="taking-performance-time-measurement-trace"></a>Realizar un seguimiento de la medición del tiempo de rendimiento

Realice estos pasos para realizar un seguimiento:

1.  Abra una ventana de comandos como administrador.
2.  Cierre la aplicación si ya se está ejecutando.
3.  Cambie los directorios al *directorio gpuview* dentro de la Windows rendimiento Toolkit carpeta.
4.  Escriba "log.cmd" para iniciar el seguimiento de eventos. Esta opción registra los eventos más interesantes. Otras opciones disponibles registra un ámbito diferente de los eventos. Por ejemplo, el modo de registro "v" o detallado captura todos los eventos que **GPUView** conoce.
5.  Inicie el ejemplo y ejecótelo de una manera que cubra la ruta de rendimiento que debe analizar.
6.  Vuelva a las ventanas de comandos y escriba de nuevo "log.cmd" para detener el registro.
7.  Esto genera un archivo denominado "merged.etl" en la *carpeta gpuview.* Puede guardar este archivo en otra ubicación y analizarlo en el mismo equipo o en otro. Para ver los detalles de la captura de pila, guarde el archivo de símbolos (.pdb) asociado a la aplicación.

## <a name="measurements"></a>Medidas


> [!Note]  
> Las medidas de la muestra de realización de geometría se toman en una máquina Quad Core con una tarjeta gráfica DirectX11 integrada. Las medidas varían en función de la configuración de la máquina.

 

En esta sección se muestra cómo medir el tiempo de inicio, el tiempo de CPU y la GPU por fotograma. Puede capturar un seguimiento del rendimiento del mismo ejemplo en la máquina y ver las diferencias en las distintas medidas.

Para analizar el seguimiento en **GPUView,** abra el archivo "merged.elt" **GPUView.exe**.

### <a name="startup-time"></a>Tiempo de inicio

El tiempo de inicio se mide por el tiempo total empleado desde el inicio de la aplicación hasta que el contenido aparece por primera vez en la pantalla.

La medida en tiempo de inicio se toma mejor siguiendo los pasos enumerados en la sección anterior con estas variaciones:

-   Si toma las medidas de inicio la primera vez que inicia la aplicación, se denomina arranque en frío. Esto puede variar con respecto a las medidas realizadas después de iniciar la aplicación varias veces en un período de tiempo pequeño. Esto se denomina inicio en caliente. Dependiendo de cuántos recursos cree una aplicación al iniciarse, puede haber una gran diferencia entre los dos tiempos de inicio. En función de los objetivos de la aplicación, puede ser conveniente medir uno u otro.
-   Al registrar la información de rendimiento, finalice la aplicación en cuanto el primer fotograma se muestre en la pantalla.

### <a name="calculating-start-up-time-using-gpuview"></a>Cálculo del tiempo de inicio mediante **GPUView**

1.  En **GPUView,** desplácese hacia abajo hasta el proceso correspondiente, en este caso, GeometryRealization.exe.

    ![Captura de pantalla que muestra un ejemplo de procesos en GPUView.](images/profile1.png)

2.  La cola de CPU de contexto representa la carga de trabajo de gráficos en cola en el hardware, pero no necesariamente la procesa el hardware. Cuando se abre el archivo de seguimiento, muestra todos los eventos registrados entre el momento en que se tomó el seguimiento. Para calcular el tiempo de inicio, seleccione la región de interés y haga zoom en la parte inicial de la primera cola de CPU de contexto (esta es la que muestra la actividad) mediante Ctrl +Z. Puede encontrar más información **sobre los controles GPUView** en la sección "Resumen de controles GPUView" del archivo de Ayuda **de GPUView.**  En la ilustración siguiente solo se muestra GeometryRealization.exe proceso de ampliación a la primera parte de la cola de CPU de contexto. El color de la cola de CPU de contexto se indica mediante el rectángulo justo debajo de la cola y los mismos paquetes de datos de color de la cola muestran el trabajo de GPU en cola en el hardware. El paquete de patrón de sombreado de la cola de contexto muestra el paquete actual, lo que significa que la aplicación quiere que el hardware presente el contenido en la pantalla.

    ![Captura de pantalla que muestra ejemplos de la "Cola de C U de contexto de C".](images/profile2.png)

3.  El tiempo de inicio es la hora a la que se inicia la aplicación por primera vez (en este caso, el módulo de punto de entrada del subproceso de interfaz de usuario SHCORE.dll) hasta el momento en que aparece por primera vez el contexto (marcado por un paquete de sombreado). En esta ilustración se resalta el área de interés.

    > [!Note]  
    > La información actual real se representa en la cola de volteo y, por tanto, el tiempo se extiende hasta que el paquete actual se completa realmente en la cola de volteo.

     

    La barra de estado completa no está visible en la ilustración siguiente, que también muestra el tiempo transcurrido entre las partes resaltadas. Este es el tiempo de inicio de la aplicación. En este caso, para la máquina mencionada anteriormente, salió en torno a 240 ms.

    ![Captura de pantalla que muestra las áreas de interés relacionadas con el tiempo de inicio en la "Cola de C P U de contexto".](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>Tiempo de CPU y GPU por fotograma

Hay que tener en cuenta algunas cosas al medir el tiempo de CPU. Busque las áreas del seguimiento en las que ha ejercicio el escenario que se va a analizar. Por ejemplo, en el ejemplo de realización de geometría, uno de los escenarios analizados es la transición entre las primitivas de representación 2048 y 8192, todas no realizadas (como en , la geometría no se tesela cada fotograma). El seguimiento muestra claramente la diferencia en la actividad de CPU y GPU antes y después de la transición en el número de primitivas.

Se están analizando dos escenarios para calcular el tiempo de CPU y GPU por fotograma. Son como se muestra a continuación.

-   Pasar de representar primitivas 2048 no realizadas a 8192 primitivas no realizadas.
-   Pasar de representar primitivas realizadas en 8192 a primitivas 8192 no realizadas.

En ambos casos, se observó que la velocidad de fotogramas se redujo drásticamente. Al medir el tiempo de CPU y GPU, la relación entre los dos, así como algunos otros patrones del seguimiento, puede proporcionar información útil sobre las áreas problemáticas de la aplicación.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Cálculo del tiempo de CPU y GPU cuando las primitivas de 2048 se representan como no realizadas

1.  Abra el archivo de seguimiento **medianteGPUView.exe**.
2.  Desplácese hacia abajo hasta GeometryRealization.exe proceso.
3.  Seleccione un área para calcular el tiempo de CPU y haga zoom en él mediante CTRL + Z.

    ![Captura de pantalla que muestra un área seleccionada para calcular la hora de C P U en la "Cola de CPU de contexto".](images/profile4.png)

4.  Mostrar información de sincronización de v al alternar entre F8. Mantener el zoom hacia dentro hasta que sea fácil ver claramente un valor de vsync de datos. Las líneas azules son donde las horas de sincronización de V. Normalmente, se producen una vez cada 16 ms (60 fps), pero si DWM encuentra un problema de rendimiento, se ejecuta más lentamente, por lo que se producirán una vez cada 32 ms (30 fps). Para obtener una idea del tiempo, seleccione de una barra azul a la siguiente y, a continuación, mire el número de ms notificados en la esquina inferior derecha de la **ventana GPUView.**

    ![Captura de pantalla que muestra un ejemplo de tiempos de sincronización de v.](images/profile5.png)

5.  Para medir el tiempo de CPU por fotograma, mida el tiempo que han llevado todos los subprocesos implicados en la representación. Puede merecer la pena restringir el subproceso que se espera que sea más relevante desde el punto de vista del rendimiento. Por ejemplo, en el ejemplo de realización de geometría, el contenido se anima y debe representarse en la pantalla cada fotograma, lo que hace que el subproceso de la interfaz de usuario sea el importante. Una vez que determine qué subproceso se va a mirar, mida la longitud de las barras de este subproceso. Si se hace un promedio de algunas de ellas, se produce tiempo de CPU por fotograma. En la ilustración siguiente se muestra el tiempo que se ha ocupado en el subproceso de la interfaz de usuario. También muestra que esta vez encaja bien entre dos sincronizaciones virtuales consecutivas, lo que significa que está alcanzando 60FPS.

    ![Captura de pantalla que muestra el tiempo que se ha ocupado en el subproceso de IA.](images/profile6.png)

    También puede comprobarlo si observa la cola de volteo para el período de tiempo correspondiente, que muestra que DWM puede presentar cada fotograma.

    ![Captura de pantalla que muestra un ejemplo de la "Cola de volteo".](images/profile7.png)

6.  El tiempo de GPU se puede medir de la misma manera que el tiempo de CPU. Haga zoom en el área pertinente como en el caso de medir el tiempo de CPU. Mida la longitud de las barras de la cola de hardware de GPU con el mismo color que el color de la cola de CPU de contexto. Siempre que las barras quepa dentro de sincronizaciones virtuales consecutivas, la aplicación se ejecuta sin problemas a 60FPS.

    ![Captura de pantalla que muestra un ejemplo de la "cola de hardware de GPU" que muestra información de que una aplicación se ejecuta a 60 F P S.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Cálculo del tiempo de CPU y GPU cuando 8192 primitivos se representan sin realizar

1.  Si vuelve a seguir los mismos pasos, el seguimiento muestra que todo el trabajo de CPU para un fotograma no cabe entre una sincronización de v y la siguiente. Esto significa que la aplicación está enlazada a la CPU. El subproceso de interfaz de usuario está saturando la CPU.

    ![Captura de pantalla que muestra un ejemplo del subproceso de interfaz de usuario que satura la U de C.](images/profile9.png)

    Si miramos la cola de volteo, también queda claro que DWM no puede presentar todos los fotogramas.

    ![Captura de pantalla que muestra un ejemplo de que D W M no puede presentar cada fotograma.](images/profile10.png)

2.  Para analizar dónde se dedica el tiempo, abra el seguimiento **en XPerf**. Para analizar el tiempo de inicio **en XPerf,** busque primero el intervalo de tiempo **en GPUView**. Mueva el mouse sobre la izquierda del intervalo y la derecha y anote el tiempo absoluto que se muestra en la parte inferior de la **ventana GPUView.** A continuación, abra el mismo archivo .etl en **XPerf** y desplácese hacia abajo hasta el gráfico "Muestreo de CPU por CPU", haga clic con el botón derecho y seleccione "Seleccionar intervalo...". Esto permite escribir el intervalo de interés que se ha detectado al mirar el seguimiento de GPU.

    ![Captura de pantalla que muestra "Muestreo de C P U por C P U" en "Windows análisis de rendimiento".](images/profile11.png)

3.  Vaya al menú Seguimiento y asegúrese de que la opción "Cargar símbolos" está activada. Además, vaya a Seguimiento -> rutas de acceso de símbolos y escriba la ruta de acceso del símbolo de la aplicación. Un archivo de símbolos contiene información de depuración sobre un ejecutable compilado en una base de datos independiente (.pdb). Este archivo se conoce normalmente como PDB. Puede encontrar más información sobre los archivos de símbolos aquí: [Archivos de símbolos](/windows/desktop/Debug/symbol-files). Este archivo se puede encontrar en la carpeta "Depurar" del directorio de la aplicación.

4.  Para obtener el desglose de dónde se pasa el tiempo en la aplicación, haga clic con el botón derecho en el intervalo seleccionado en el paso anterior y haga clic en Tabla de resumen. Para obtener información general sobre cuánto tiempo se pasa en cada archivo DLL, desactive "Pila" en el menú "Columnas". Tenga en cuenta que la columna "Count" aquí muestra cuántos ejemplos hay dentro de la dll o función especificadas. Dado que se toma aproximadamente una muestra por ms, este número se puede usar como una mejor suposición de cuánto tiempo se emplea en cada archivo DLL o función. Al comprobar la "Pila" en el menú Columnas, se ofrece el tiempo inclusivo empleado en cada función del gráfico de llamadas. Esto le ayudará a dividir aún más los puntos del problema.

5.  La información de seguimiento de pila para primitivas no realizadas de 2048 revela que el 30 % del tiempo de CPU se dedica al proceso de realización de geometría. De eso, aproximadamente el 36 % del tiempo se dedica a la teselación y acariciamiento de geometría.

6.  La información de seguimiento de pila para primitivas 8192 no realizadas revela que aproximadamente el 60 % del tiempo de CPU (4 núcleos) se dedica a la realización de geometría.

    ![Captura de pantalla que muestra información de seguimiento de pila para la hora de C P U.](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Calcular el tiempo de CPU cuando se realizan las primitivas 8192

En los perfiles se puede ver claramente que la aplicación está enlazada a la CPU. Para reducir el tiempo empleado por la CPU, las geometrías se pueden crear una vez y almacenarse en caché. El contenido almacenado en caché se puede representar en cada fotograma sin incurrir en el costo de teselación de geometría por fotograma. Al mirar el seguimiento en **GPUView** para la parte realizada de la aplicación, está claro que DWM es capaz de presentar cada fotograma y el tiempo de CPU se ha reducido drásticamente.

![Captura de pantalla que muestra un ejemplo de un seguimiento en GPUView que muestra que D W M puede presentar cada fotograma.](images/profile13.png)

La primera parte del gráfico muestra 8192 primitivas realizadas. El tiempo de CPU correspondiente por fotograma puede caber dentro de dos sincronizaciones virtuales consecutivas. En la parte posterior del gráfico, esto no es cierto.

Si se **busca en XPerf,** la CPU está inactiva durante el tiempo más largo con solo aproximadamente el 25 % del tiempo de CPU dedicado a la aplicación de realización de geometría.

![Captura de pantalla de gpuview.](images/profile14.png)

## <a name="summary"></a>Resumen

**GPUView y** **XPerf y** herramientas eficaces para analizar el rendimiento de las aplicaciones de [DirectX.](/previous-versions/windows/apps/jj262109(v=win.10)) Este artículo es una introducción para usar estas herramientas y comprender las medidas de rendimiento básicas y las características de la aplicación. Además de comprender el uso de herramientas, primero es importante comprender la aplicación que se está analizando. Comience con la búsqueda de respuestas a preguntas como ¿qué está intentando lograr la aplicación? ¿Qué subprocesos del sistema son más importantes? ¿Cuáles son los descuentos que está dispuesto a realizar? Al analizar los seguimientos de rendimiento, empiece por mirar los lugares problemáticos obvios. ¿Está enlazada la CPU o la GPU de la aplicación? ¿La aplicación puede presentar cada fotograma? Las herramientas junto con una comprensión de la aplicación pueden proporcionar información muy útil para comprender, encontrar y resolver finalmente problemas de rendimiento.

 

 