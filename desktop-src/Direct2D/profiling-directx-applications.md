---
title: Generación de perfiles de aplicaciones de DirectX
description: Muestra cómo medir algunas de las medidas de tiempo de rendimiento más importantes para una aplicación DirectX mediante las herramientas XPerf y GPUView que se incluyen como parte del kit de herramientas de rendimiento de Windows.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0280389d4f8f2161e5e07f8906df7ea0484ad458
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571015"
---
# <a name="profiling-directx-apps"></a>Generación de perfiles de aplicaciones de DirectX

Esto muestra cómo medir algunas de las medidas de tiempo de rendimiento más importantes para una aplicación [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) mediante las herramientas **XPerf** y **GPUView** que se incluyen como parte del kit de herramientas de rendimiento de Windows. Esta no es una guía completa para comprender las herramientas, sino su aplicabilidad específica para analizar el rendimiento de las aplicaciones de DirectX. Aunque la mayoría de las técnicas descritas aquí son relevantes para todas las aplicaciones de DirectX, es más importante para las aplicaciones que usan cadenas de intercambio y no para las aplicaciones de DirectX basadas en XAML que usan SIS/VSI y animaciones XAML. Le guiaremos a través de las mediciones clave de tiempo de rendimiento, la adquisición e instalación de las herramientas y la realización de seguimientos de medición del rendimiento y su análisis para comprender los cuellos de botella de la aplicación.

## <a name="about-the-tools"></a>Acerca de las herramientas

### <a name="xperf"></a>**XPerf**

**XPerf** es un conjunto de herramientas de análisis de rendimiento basadas en el seguimiento de eventos para Windows (ETW) diseñado para medir y analizar el rendimiento y el uso de recursos detallados del sistema y la aplicación. A partir de Windows 8, esta herramienta de línea de comandos tiene una interfaz gráfica de usuario y se denomina Windows performance Recorder (WPR) y Windows Performance Analyzer (WPA). Puede encontrar más información sobre estas herramientas en la Página Web de [Windows performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): [Windows performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

ETW recopila eventos de kernel solicitados y los guarda en un archivo denominado archivo de registro de seguimiento de eventos (ETL). Estos eventos de kernel proporcionan una amplia información sobre una aplicación y las características del sistema cuando se ejecuta la aplicación. Los datos se recopilan mediante la habilitación de la captura de seguimiento, la realización del escenario de aplicación deseado que necesita análisis y la detención de la captura, que guarda los datos en un archivo ETL. A continuación, puede analizar el archivo en el mismo equipo o en otro diferente mediante la herramienta de línea de comandos **xperf.exe** o la herramienta de análisis de seguimiento visual **xperfview.exe**.

### <a name="gpuview"></a>GPUView

**GPUView** es una herramienta de desarrollo para determinar el rendimiento de la unidad de procesamiento de gráficos (GPU) y la CPU. Observa el rendimiento con respecto al procesamiento de búfer de acceso directo a memoria (DMA) y el resto del procesamiento de vídeo en el hardware de vídeo.

En el caso de las aplicaciones de [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) que dependen en gran medida de la GPU, **GPUView** es una herramienta eficaz para comprender la relación entre el trabajo realizado en la CPU y la GPU. Para obtener más información sobre **GPUView**, consulte [uso de GPUView](/windows-hardware/drivers/display/using-gpuview).

De forma similar a **XPerf**, primero se toma un seguimiento de ETW iniciando el servicio de seguimiento, ejercitando el escenario en el que se debe tener en cuenta el análisis de la aplicación, deteniendo el servicio y guardando la información en un archivo ETL. **GPUView** presenta los datos presentes en el archivo ETL en un formato gráfico.

Después de instalar la herramienta **GPUView** , se recomienda leer el tema "presentación principal de **GPUView**" en el menú "ayuda de **GPUView** ". Contiene información útil sobre cómo interpretar la interfaz de usuario de **GPUView** .

## <a name="installing-the-tools"></a>Instalación de las herramientas

Tanto **XPerf** como **GPUView** se incluyen en el kit de herramientas de rendimiento de Windows (WPT).

**XPerf** se distribuye como parte del kit de desarrollo de software (SDK) de Windows para Windows. [Descargue el Windows SDK](https://dev.windows.com/downloads).

**GPUView** está disponible en Windows Assessment and Deployment Kit (Windows ADK). [Descargue Windows ADK](/windows-hardware/get-started/adk-install).

Después de la instalación, debe agregar los directorios que contienen **XPerf** y **GPUView** a la variable del sistema "path".

Haga clic en el botón Inicio y escriba "variables del sistema". Se abre el ventana Propiedades del sistema. Haga clic en "editar las variables de entorno del sistema". Seleccione "variables de entorno" en el cuadro de diálogo "propiedades del sistema". La variable "path" se encuentra en "variables del sistema". Anexe el directorio que contiene **xperf.exe** y **GPUView.exe** a la ruta de acceso. Estos ejecutables se encuentran en el directorio "Windows performance Toolkit" dentro de "kits de Windows". La ubicación predeterminada es: **C: \\ archivos de programa (x86) \\ kits de Windows \\ 10 \\ Windows performance Toolkit**.

## <a name="performance-time-measurements"></a>Medidas de tiempo de rendimiento

La mayoría de las aplicaciones esperan ejecutarse sin problemas y responder a los datos proporcionados por el usuario. Sin embargo, en función del escenario que desee, un aspecto de rendimiento podría ser más importante que otro. Por ejemplo, en el caso de una aplicación de lector de noticias que se ejecuta en un Touch Tablet PC, el aspecto más importante es ver un solo artículo a la vez y desplazarse por el mismo artículo u otro distinto. En este escenario, la capacidad de representar todo el contenido de cada fotograma no es necesario. Sin embargo, la capacidad de desplazarse por el artículo sin problemas en un gesto táctil es muy importante.

En otra instancia, un juego o una aplicación de representación de vídeo que usa muchas animaciones tiene problemas si se quitan los fotogramas. En este caso, la capacidad de presentar contenido en la pantalla sin interuption de los datos proporcionados por el usuario es muy importante.

Para comprender qué parte de la aplicación es problemática, el primer paso es decidir los escenarios más importantes. Una vez que se comprenden los aspectos básicos de la aplicación y cómo se van a ejercitar, es más fácil buscar problemas con las herramientas.

Algunas de las métricas de tiempo de rendimiento más comunes son las siguientes:

### <a name="startup-time"></a>Tiempo de inicio

Tiempo medido desde el inicio del proceso hasta que se llega a la pantalla. Esta medida es más útil cuando el sistema está caliente, lo que significa que la medición se realiza una vez que se inicia la aplicación varias veces.

### <a name="cpu-time-per-frame"></a>Tiempo de CPU por fotograma

El tiempo durante el cual la CPU procesa activamente la carga de trabajo de la aplicación para un fotograma. Si la aplicación se ejecuta sin problemas, todo el procesamiento necesario para un fotograma se produce dentro de un intervalo de sincronización de v. Con la frecuencia de actualización del monitor de 60 Hz, esto llega a 16ms estándar por fotograma. Si el tiempo de CPU o el marco es mayor que 16ms estándar, es posible que se necesiten optimizaciones de la CPU para producir una experiencia de aplicación sin problemas.

### <a name="gpu-time-per-frame"></a>Tiempo de GPU por fotograma

El tiempo durante el cual la GPU procesa activamente la carga de trabajo de la aplicación para un fotograma. Una aplicación está enlazada por GPU cuando el tiempo que se tarda en procesar el valor de los datos de un fotograma es superior a 16ms estándar.

Poder comprender si una aplicación es un límite de CPU o GPU limitará la parte problemática del código.

## <a name="taking-performance-time-measurement-trace"></a>Seguimiento de medición de tiempo de rendimiento

Siga estos pasos para realizar un seguimiento:

1.  Abra una ventana de comandos como administrador.
2.  Cierre la aplicación si ya se está ejecutando.
3.  Cambie los directorios al directorio *gpuview* dentro de la carpeta Windows performance Toolkit.
4.  Escriba "log. cmd" para iniciar el seguimiento de eventos. Esta opción registra los eventos más interesantes. Otras opciones disponibles registran el ámbito de los eventos. Por ejemplo, ' v ' o el modo de registro detallado captura todos los eventos de los que **GPUView** es consciente.
5.  Inicie el ejemplo y ejecute el ejemplo de forma que cubra la ruta de rendimiento que necesita analizar.
6.  Vuelva a las ventanas de comandos y escriba "log. cmd" de nuevo para detener el registro.
7.  Esto genera un archivo llamado "Merged. ETL" en la carpeta *gpuview* . Puede guardar este archivo en otra ubicación y puede analizarlo en el mismo equipo o en otro diferente. Para ver los detalles de la captura de la pila, guarde el archivo de símbolos (. pdb) asociado a la aplicación.

## <a name="measurements"></a>Medidas


> [!Note]  
> El ejemplo de medición de la realización de geometría se realiza en un equipo de cuatro núcleos con una tarjeta gráfica de DirectX11 integrada. Las medidas varían en función de la configuración de la máquina.

 

En esta sección se muestra cómo medir el tiempo de inicio, la CPU y la hora de GPU por medida de fotogramas. Puede capturar un seguimiento de rendimiento para el mismo ejemplo en la máquina y ver las diferencias en las distintas mediciones.

Para analizar el seguimiento en **GPUView**, abra el archivo "Merged. ELT" mediante **GPUView.exe**.

### <a name="startup-time"></a>Tiempo de inicio

El tiempo de inicio se mide por el tiempo total transcurrido desde el inicio de la aplicación hasta que el contenido aparece por primera vez en la pantalla.

La medida de tiempo de inicio se realiza mejor siguiendo los pasos indicados en la sección anterior con estas variaciones:

-   Si realiza las medidas de inicio la primera vez que inicia la aplicación, se denomina Inicio en frío. Esto puede variar de las medidas tomadas después de iniciar la aplicación varias veces en poco tiempo. Esto se denomina Inicio en caliente. En función del número de recursos que cree una aplicación en el inicio, puede haber una gran diferencia entre los dos tiempos de inicio. En función de los objetivos de la aplicación, puede ser conveniente medir uno u otro.
-   Al registrar la información de rendimiento, finalice la aplicación en cuanto el primer fotograma se muestre en la pantalla.

### <a name="calculating-start-up-time-using-gpuview"></a>Calcular el tiempo de inicio mediante **GPUView**

1.  En **GPUView**, desplácese hacia abajo hasta el proceso correspondiente, en este caso GeometryRealization.exe.

    ![Captura de pantalla que muestra un ejemplo de procesos en GPUView.](images/profile1.png)

2.  La cola de la CPU de contexto representa la carga de trabajo de gráficos en cola en el hardware, pero no necesariamente la procesa el hardware. Cuando se abre el archivo de seguimiento, muestra todos los eventos registrados entre el momento en que se tomó el seguimiento. Para calcular el tiempo de inicio, seleccione la región de interés, acerque la parte inicial de la primera cola de la CPU de contexto (es la que muestra la actividad) mediante Ctrl + Z. Puede encontrar más información sobre los controles de **GPUView** en la sección del archivo de ayuda de **GPUView** "Summary of **GPUView** Controls". En la siguiente ilustración solo se muestra el proceso de GeometryRealization.exe de zoom en la primera parte de la cola de la CPU de contexto. El color de la cola de la CPU de contexto se indica mediante el rectángulo que se encuentra justo debajo de la cola y los mismos paquetes de datos de color en la cola muestran el trabajo de GPU en cola en el hardware. El paquete del patrón de trama en la cola de contexto muestra el paquete presente, lo que significa que la aplicación desea que el hardware presente el contenido en la pantalla.

    ![Captura de pantalla que muestra ejemplos de la ' contexto C P U la cola '.](images/profile2.png)

3.  La hora de inicio es la hora a la que se inicia la aplicación por primera vez (en este caso, el módulo de punto de entrada del subproceso de interfaz de usuario SHCORE.dll) hasta la hora en que el contexto aparece por primera vez (marcado por un paquete de trama). En la ilustración se resalta el área de interés.

    > [!Note]  
    > La información actual actual se representa en la cola de volteo y, por lo tanto, el tiempo que se tarda se extiende hasta que el paquete actual se completa realmente en la cola de volteo.

     

    La barra de estado completa no está visible en la ilustración siguiente, que también muestra el tiempo transcurrido entre las partes resaltadas. Este es el tiempo de inicio de la aplicación. En este caso, para la máquina mencionada anteriormente, llegó a estar alrededor de 240ms.

    ![Captura de pantalla que muestra las áreas de interés con respecto al tiempo de inicio en el "contexto C P U la cola".](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>Tiempo de CPU y GPU por fotograma

Hay algunos aspectos que se deben tener en cuenta al medir el tiempo de CPU. Busque las áreas del seguimiento en las que ha ejecutado el escenario que se va a analizar. Por ejemplo, en el ejemplo de realización de geometría, uno de los escenarios que se han analizado es la transición entre la representación de primitivos 2048 y 8192, todo no realizado (como en, Geometry no se tesela cada fotograma). El seguimiento muestra claramente la diferencia en la actividad de la CPU y la GPU antes y después de la transición en el número de primitivas.

Se están analizando dos escenarios para calcular el tiempo de la CPU y la GPU por fotograma. Son los siguientes:

-   Transición de la representación de 2048 primitivos no reales a 8192 primitivas no realizadas.
-   Transición de la representación de 8192 de primitivas realizadas a 8192 primitivas no realizadas.

En ambos casos, se observó que la velocidad de fotogramas se ha quitado drásticamente. Medida de la CPU y la hora de la GPU, la relación entre los dos y otros patrones del seguimiento puede proporcionar información útil sobre las áreas problemáticas de la aplicación.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Calcular la hora de la CPU y la GPU en que se representan los 2048 primitivos no reales

1.  Abra el archivo de seguimiento mediante **GPUView.exe**.
2.  Desplácese hacia abajo hasta el proceso de GeometryRealization.exe.
3.  Seleccione un área para calcular el tiempo de CPU y haga zoom en ella con CTRL + Z.

    ![Captura de pantalla que muestra un área seleccionada para calcular el tiempo de U U hora de C en la ' cola de la CPU de contexto '.](images/profile4.png)

4.  Muestre la información de la sincronización de v alternando entre F8. Mantener el zoom hasta que sea fácil ver claramente un valor de VSYNC de los datos. Las líneas azules son los tiempos de sincronización de v. Normalmente, estos errores se producen una vez cada 16 ms (60 fps), pero si DWM detecta un problema de rendimiento, se ejecuta más lentamente, por lo que se producirá una vez cada 32 ms (30 fps). Para obtener un intervalo de tiempo, seleccione una barra azul hasta la siguiente y, a continuación, examine el número de MS indicado en la esquina inferior derecha de la ventana **GPUView** .

    ![Captura de pantalla que muestra un ejemplo de tiempos de sincronización de v.](images/profile5.png)

5.  Para medir el tiempo de CPU por fotograma, mida el tiempo que tardan todos los subprocesos implicados en la representación. Podría merecer la pena limitar el subproceso que se espera que sea más relevante desde el punto de vista del rendimiento. Por ejemplo, en el ejemplo de realización de geometría, el contenido se anima y debe representarse en la pantalla cada fotograma que hace que el subproceso de la interfaz de usuario sea el importante. Una vez que determine el subproceso que se va a examinar, mida la longitud de las barras en este subproceso. Al calcular el promedio de algunos de estos se produce el tiempo de CPU por fotograma. En la ilustración siguiente se muestra el tiempo invertido en el subproceso de la interfaz de usuario. También muestra que este tiempo se ajusta bien entre dos sincronizaciones v consecutivas, lo que significa que está llegando a 60FPS.

    ![Captura de pantalla que muestra el tiempo que se tarda en el subproceso U I.](images/profile6.png)

    También puede comprobar observando la cola de volteo para el período de tiempo correspondiente, que muestra que DWM puede presentar cada fotograma.

    ![Captura de pantalla que muestra un ejemplo de la ' Flip Queue '.](images/profile7.png)

6.  La hora de la GPU se puede medir de la misma manera que el tiempo de CPU. Acerque el área relevante como en el caso de medir el tiempo de CPU. Mida la longitud de las barras en la cola de hardware de GPU con el mismo color que el color de la cola de la CPU de contexto. Siempre que las barras quepan en las sincronizaciones de v consecutivas, la aplicación se ejecuta sin problemas en 60FPS.

    ![Captura de pantalla que muestra un ejemplo de la "cola de hardware de GPU" que muestra la información que una aplicación se está ejecutando en 60 F P S.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Calcular la hora de la CPU y la GPU en que se representan los 8192 primitivos no reales

1.  Si sigue los mismos pasos de nuevo, el seguimiento muestra que todo el trabajo de CPU de un fotograma no se ajusta a una sincronización v y a la siguiente. Esto significa que la aplicación está enlazada a la CPU. El subproceso de la interfaz de usuario está saturando la CPU.

    ![Captura de pantalla que muestra un ejemplo del subproceso de interfaz de usuario que satura la U de C P.](images/profile9.png)

    Al examinar la cola de volteo, también está claro que DWM no puede presentar cada fotograma.

    ![Captura de pantalla que muestra un ejemplo de D W M no se puede presentar cada fotograma.](images/profile10.png)

2.  Para analizar dónde se está dedicando el tiempo, abra el seguimiento en **XPerf**. Para analizar el tiempo de inicio en **XPerf**, busque primero el intervalo de tiempo en **GPUView**. Pasar el mouse por encima de la izquierda del intervalo y la derecha y tomar nota del tiempo absoluto que se muestra en la parte inferior de la ventana de **GPUView** . A continuación, abra el mismo archivo. ETL en **XPerf** y, desplácese hacia abajo hasta el gráfico "muestreo de la CPU por CPU", haga clic con el botón derecho y seleccione "seleccionar intervalo...". Esto permite escribir en el intervalo de interés que se descubrió examinando el seguimiento de la GPU.

    ![Captura de pantalla que muestra ' C P U muestreo por C P U ' en ' análisis de rendimiento de Windows '.](images/profile11.png)

3.  Vaya al menú de seguimiento y asegúrese de que la opción "cargar símbolos" está activada. Además, vaya a seguimiento-> configurar rutas de acceso de símbolos y escriba la ruta de acceso de símbolos de la aplicación. Un archivo de símbolos contiene información de depuración sobre un ejecutable compilado en una base de datos independiente (. pdb). Este archivo se conoce comúnmente como PDB. Encontrará más información sobre los archivos de símbolos aquí: [archivos de símbolos](/windows/desktop/Debug/symbol-files). Este archivo puede encontrarse en la carpeta "debug" del directorio de la aplicación.

4.  Para obtener el desglose de la hora en que se está empleando la aplicación, haga clic con el botón derecho en el intervalo seleccionado en el paso anterior y haga clic en tabla de resumen. Para obtener una visión general de cuánto tiempo se dedica a cada archivo dll, desactive "pila" en el menú "columnas". Observe que en la columna "recuento" se muestra el número de muestras que se encuentran dentro de la función o el archivo dll especificados. Dado que se toma aproximadamente un ejemplo por MS, este número puede usarse como una mejor aproximación a la cantidad de tiempo empleado en cada archivo dll o función. Al activar la "pila" en el menú columnas, se proporcionará el tiempo inclusivo invertido en cada función del gráfico de llamadas. Esto le ayudará a desglosar aún más los puntos problemáticos.

5.  La información de seguimiento de la pila de 2048 primitivas no realizadas revela que el 30% del tiempo de CPU se emplea en el proceso de realización de geometría. De eso alrededor del 36% del tiempo se dedica a la teselación geométrica y al trazado.

6.  La información de seguimiento de la pila de 8192 primitivas no realizadas revela que alrededor del 60% del tiempo de CPU (4 núcleos) se emplea en la realización de la geometría.

    ![Captura de pantalla que muestra información de seguimiento de la pila para el tiempo de C P U.](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Calcular el tiempo de CPU cuando se representan los 8192 primitivos

Está claro de los perfiles a los que la aplicación está enlazada a la CPU. Con el fin de reducir el tiempo invertido por la CPU, se pueden crear geometrías una vez y almacenarse en caché. El contenido almacenado en caché se puede representar en cada fotograma sin incurrir en el costo de teselación de geometría por fotograma. Al examinar el seguimiento en **GPUView** para la parte de la aplicación que se ha realizado, es evidente que DWM puede presentar cada fotograma y el tiempo de CPU ha disminuido drásticamente.

![Captura de pantalla que muestra un ejemplo de un seguimiento en GPUView que muestra D W M puede presentar cada fotograma.](images/profile13.png)

La primera parte del gráfico muestra las primitivas 8192 realizadas. El tiempo de CPU correspondiente por fotograma puede caber en dos sincronizaciones v consecutivas. En la parte posterior del gráfico, esto no es cierto.

Al buscar en **XPerf**, la CPU está en estado inactivo durante el tiempo más largo con solo un 25% del tiempo de CPU dedicado a la aplicación de realización de geometría.

![captura de pantalla gpuview.](images/profile14.png)

## <a name="summary"></a>Resumen

Tanto **GPUView** como **XPerf** como herramientas eficaces para analizar el rendimiento de las aplicaciones de [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) . Este artículo es una guía básica para el uso de estas herramientas y la comprensión de las medidas de rendimiento y las medidas de aplicación básicas. Además de comprender el uso de las herramientas, es importante comprender la aplicación que se está analizando. Comience a buscar respuestas a preguntas como ¿qué es la aplicación que está intentando lograr? ¿Qué subprocesos del sistema son más importantes? ¿Cuáles son las ventajas y desventajas que tiene que hacer? Al analizar los seguimientos de rendimiento, empiece por mirar en lugares problemáticos obvios. ¿El límite de la CPU o la GPU de la aplicación? ¿La aplicación puede presentar cada fotograma? Las herramientas, junto con una descripción de la aplicación, pueden proporcionar información muy útil al comprender, buscar y, por último, resolver problemas de rendimiento.

 

 