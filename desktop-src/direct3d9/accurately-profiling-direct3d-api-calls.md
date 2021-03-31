---
description: Una vez que tiene una aplicación de Microsoft Direct3D funcional y desea mejorar su rendimiento, por lo general se usa una herramienta de generación de perfiles estándar o alguna técnica de medición personalizada para medir el tiempo que se tarda en ejecutar una o varias llamadas de la interfaz de programación de aplicaciones (API). Si lo ha hecho pero está obteniendo resultados de control de tiempo que varían de una secuencia de representación a la siguiente, o si está creando supuestos que no contengan resultados reales del experimento, la siguiente información puede ayudarle a entender por qué.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Generación precisa de perfiles de llamadas de la API de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb6d60fcc1b3ace4112dbf7028d91e2c9c8b345
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807705"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Generación precisa de perfiles de llamadas de la API de Direct3D (Direct3D 9)

-   [La generación de perfiles de Direct3D con precisión es difícil](#accurately-profiling-direct3d-is-difficult)
-   [Cómo generar perfiles de una secuencia de representación de Direct3D con precisión](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Generar perfiles de cambios de estado de Direct3D](#profiling-direct3d-state-changes)
-   [Resumen](#summary)
-   [ICE](#appendix)

Una vez que tiene una aplicación de Microsoft Direct3D funcional y desea mejorar su rendimiento, por lo general se usa una herramienta de generación de perfiles estándar o alguna técnica de medición personalizada para medir el tiempo que se tarda en ejecutar una o varias llamadas de la interfaz de programación de aplicaciones (API). Si lo ha hecho pero está obteniendo resultados de control de tiempo que varían de una secuencia de representación a la siguiente, o si está creando supuestos que no contengan resultados reales del experimento, la siguiente información puede ayudarle a entender por qué.

La información que se proporciona aquí se basa en el supuesto de que tiene conocimientos y experiencia con lo siguiente:

-   Programación con C/C++
-   Programación de la API de Direct3D
-   Medición del tiempo de API
-   La tarjeta de vídeo y su controlador de software
-   Resultados inexplicables posibles de la experiencia de generación de perfiles anterior

## <a name="accurately-profiling-direct3d-is-difficult"></a>La generación de perfiles de Direct3D con precisión es difícil

Un generador de perfiles informa sobre la cantidad de tiempo empleado en cada llamada API. Esto se hace para mejorar el rendimiento mediante la búsqueda y la optimización de las zonas activas. Hay diferentes tipos de perfiles y técnicas de generación de perfiles.

-   Un generador de perfiles de muestreo se encuentra inactivo gran parte del tiempo, reactivando a intervalos específicos para muestrear (o registrar) las funciones que se están ejecutando. Devuelve el porcentaje de tiempo invertido en cada llamada. Por lo general, un generador de perfiles de muestreo no es muy invasivo en la aplicación y tiene un impacto mínimo en la sobrecarga de la aplicación.
-   Un generador de perfiles de instrumentación mide el tiempo real necesario para que se devuelva una llamada. Requiere la compilación de delimitadores de inicio y detención en una aplicación. Un generador de perfiles de instrumentación es comparativamente más invasivo en una aplicación que un generador de perfiles de muestreo.
-   También es posible usar una técnica de generación de perfiles personalizada con un temporizador de alto rendimiento. Esto produce resultados muy parecidos a un generador de perfiles de instrumentación.

El tipo de generador de perfiles o la técnica de generación de perfiles que se usa es solo parte del desafío de generar medidas precisas.

La generación de perfiles proporciona respuestas que le ayudan a mejorar el rendimiento. Por ejemplo, supongamos que sabe que una llamada API realiza un promedio de 1000 ciclos de reloj para ejecutarse. Puede afirmar algunas conclusiones sobre el rendimiento, como las siguientes:

-   Una CPU de 2 GHz (que pasa el 50 por ciento de su representación de tiempo) se limita a llamar a esta API 1 millón veces por segundo.
-   Para lograr 30 fotogramas por segundo, no se puede llamar a esta API más de 33.000 veces por fotograma.
-   Solo puede representar 3.3 K objetos por fotograma (suponiendo 10 de estas llamadas de API para la secuencia de representación de cada objeto).

En otras palabras, si tuviera tiempo suficiente por cada llamada API, podría responder a una pregunta de presupuesto como el número de primitivas que se pueden representar de forma interactiva. Sin embargo, los números sin procesar devueltos por un generador de perfiles de instrumentación no responderán con precisión a las preguntas de presupuesto. Esto se debe a que la canalización de gráficos tiene problemas de diseño complejos, como el número de componentes que deben realizarse, el número de procesadores que controlan cómo fluye el trabajo entre los componentes y las estrategias de optimización implementadas en tiempo de ejecución y en un controlador que están diseñados para mejorar la eficacia de la canalización.

### <a name="each-api-call-goes-through-several-components"></a>Cada llamada API atraviesa varios componentes

Varios componentes procesan cada llamada desde la aplicación a la tarjeta de vídeo. Por ejemplo, considere la siguiente secuencia de representación que contiene dos llamadas para dibujar un solo triángulo:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



En el siguiente diagrama conceptual se muestran los distintos componentes a través de los que deben pasar las llamadas.

![diagrama de componentes gráficos a los que pasan las llamadas API](images/microbenchmarkinstructionflow2.png)

La aplicación invoca Direct3D que controla la escena, controla las interacciones del usuario y determina cómo se realiza la representación. Todo este trabajo se especifica en la secuencia de representación, que se envía al tiempo de ejecución mediante llamadas a la API de Direct3D. La secuencia de representación es prácticamente independiente del hardware (es decir, las llamadas a la API son independientes del hardware, pero una aplicación tiene conocimiento de las características que admite una tarjeta de vídeo).

El tiempo de ejecución convierte estas llamadas en un formato independiente del dispositivo. El tiempo de ejecución controla toda la comunicación entre la aplicación y el controlador, de modo que una aplicación se ejecutará en más de un elemento de hardware compatible (dependiendo de las características requeridas). Al medir una llamada de función, un generador de perfiles de instrumentación mide el tiempo invertido en una función, así como el tiempo que la función devuelve. Una limitación de un generador de perfiles de instrumentación es que es posible que no incluya el tiempo necesario para que un controlador envíe el trabajo resultante a la tarjeta de vídeo ni el tiempo para que la tarjeta de vídeo procese el trabajo. En otras palabras, un generador de perfiles de instrumentación fuera del estante no puede atribuir todo el trabajo asociado a cada llamada de función.

El controlador de software usa conocimiento específico del hardware sobre la tarjeta de vídeo para convertir los comandos independientes del dispositivo en una secuencia de comandos de tarjeta de vídeo. Los controladores también pueden optimizar la secuencia de comandos que se envían a la tarjeta de vídeo, de modo que la representación en la tarjeta de vídeo se realiza de forma eficaz. Estas optimizaciones pueden provocar problemas de generación de perfiles porque la cantidad de trabajo realizada no es lo que parece ser (es posible que tenga que conocer las optimizaciones que deben tener en cuenta). Normalmente, el controlador devuelve el control al tiempo de ejecución antes de que la tarjeta de vídeo haya terminado de procesar todos los comandos.

La tarjeta de vídeo realiza la mayoría de las representaciones mediante la combinación de datos de los búferes de vértices y de índices, las texturas, la información de estado de representación y los comandos de gráficos. Cuando finaliza la representación de la tarjeta de vídeo, se completa el trabajo creado a partir de la secuencia de representación.

Cada componente (el tiempo de ejecución, el controlador y la tarjeta de vídeo) debe procesar cada llamada de la API de Direct3D para representar cualquier cosa.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Hay más de un procesador que controla los componentes

La relación entre estos componentes es aún más compleja, ya que la aplicación, el tiempo de ejecución y el controlador se controlan mediante un procesador y la tarjeta de vídeo se controla mediante un procesador independiente. En el diagrama siguiente se muestran dos tipos de procesadores: una unidad de procesamiento central (CPU) y una unidad de procesamiento de gráficos (GPU).

![diagrama de una CPU y una GPU y sus componentes](images/microbenchmarkprocessors.png)

Los sistemas de PC tienen al menos una CPU y una GPU, pero pueden tener más de uno o ambos. Las CPU se encuentran en la placa base y las GPU se encuentran en la placa base o en la tarjeta de vídeo. La velocidad de la CPU viene determinada por un chip de reloj de la placa base y la velocidad de la GPU viene determinada por un chip de reloj independiente. El reloj de la CPU controla la velocidad del trabajo realizado por la aplicación, el tiempo de ejecución y el controlador. La aplicación envía trabajo a la GPU a través del tiempo de ejecución y del controlador.

La CPU y la GPU generalmente se ejecutan a velocidades diferentes, independientes entre sí. La GPU puede responder al trabajo en cuanto el trabajo esté disponible (suponiendo que la GPU haya terminado de procesar el trabajo anterior). El trabajo de la GPU se realiza en paralelo con el trabajo de CPU resaltado por la línea curva de la ilustración anterior. Generalmente, un generador de perfiles mide el rendimiento de la CPU, no de la GPU. Esto hace que la generación de perfiles sea desafiante, ya que las medidas realizadas por un generador de perfiles de instrumentación incluyen el tiempo de CPU, pero pueden no incluir la hora de la GPU.

El propósito de la GPU es descargar el procesamiento de la CPU a un procesador diseñado específicamente para el trabajo de gráficos. En las tarjetas de vídeo modernas, la GPU reemplaza gran parte del trabajo de transformación y de iluminación de la canalización de la CPU a la GPU. Esto reduce en gran medida la carga de trabajo de la CPU, lo que deja más ciclos de CPU disponibles para otro procesamiento. Para optimizar una aplicación gráfica para un rendimiento máximo, debe medir el rendimiento de la CPU y la GPU, y equilibrar el trabajo entre los dos tipos de procesadores.

En este documento no se tratan los temas relacionados con la medición del rendimiento de la GPU o el equilibrio del trabajo entre la CPU y la GPU. Si desea comprender mejor el rendimiento de una GPU (o una tarjeta de vídeo determinada), visite el sitio web del proveedor para buscar más información sobre el rendimiento de la GPU. En su lugar, este documento se centra en el trabajo realizado por el tiempo de ejecución y el controlador reduciendo el trabajo de la GPU a una cantidad insignificante. En parte, esto se basa en la experiencia con la que las aplicaciones que experimentan problemas de rendimiento suelen estar limitadas por la CPU.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Las optimizaciones en tiempo de ejecución y controladores pueden enmascarar las medidas de API

El motor en tiempo de ejecución tiene una optimización de rendimiento integrada que puede sobrecargar la medición de una llamada individual. Este es un escenario de ejemplo que muestra este problema. Considere la siguiente secuencia de representación:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Ejemplo 1: secuencia de representación simple

Si se examinan los resultados de las dos llamadas en la secuencia de representación, un generador de perfiles de instrumentación podría devolver resultados similares a los siguientes:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



El generador de perfiles devuelve el número de ciclos de CPU necesarios para procesar el trabajo asociado a cada llamada (Recuerde que la GPU no se incluye en estos números porque la GPU todavía no ha empezado a trabajar en estos comandos). Dado que [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) requirieron casi un millón de ciclos para procesar, podría concluir que no es muy eficaz. Sin embargo, pronto verá por qué esta conclusión es incorrecta y cómo puede generar resultados que se pueden usar para el presupuesto.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>La medición de los cambios de estado requiere secuencias de representación cuidadosas

Todas las llamadas que no sean [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)o [**Clear**](/windows/desktop/api) (como [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**SetVertexDeclaration**](/windows/desktop/api)y [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) producen un cambio de estado. Cada cambio de Estado establece el estado de la canalización que controla cómo se realizará la representación.

Las optimizaciones en tiempo de ejecución y/o el controlador están diseñadas para acelerar la representación reduciendo la cantidad de trabajo necesario. A continuación se muestran un par de optimizaciones de cambio de estado que pueden contaminar los promedios de perfil:

-   Un controlador (o el Runtime) puede guardar un cambio de estado como estado local. Dado que el controlador podría funcionar en un algoritmo "diferido" (pospuesto el trabajo hasta que sea absolutamente necesario), el trabajo asociado a algunos cambios de estado podría retrasarse.
-   El tiempo de ejecución (o un controlador) puede quitar los cambios de estado mediante la optimización. Un ejemplo de esto podría ser quitar un cambio de estado redundante que deshabilita la iluminación porque la iluminación se ha deshabilitado previamente.

No hay ninguna manera infalible de examinar una secuencia de representación y concluir qué cambios de estado establecerán un bit sucio y diferirá el trabajo, o simplemente se quitarán por optimización. Aunque pueda identificar los cambios de estado optimizados en el entorno de ejecución o el controlador de hoy, es probable que se actualice el entorno en tiempo de ejecución o el controlador de mañana. Tampoco sabe fácilmente cuál era el estado anterior, por lo que es difícil identificar los cambios de estado redundantes. La única manera de comprobar el costo de un cambio de estado es medir la secuencia de representación que incluye los cambios de estado.

Como puede ver, las complicaciones ocasionadas por tener varios procesadores, los comandos que se procesan en más de un componente y las optimizaciones integradas en los componentes dificultan la predicción de la generación de perfiles. En la sección siguiente, se abordará cada uno de estos desafíos de generación de perfiles. Se mostrarán las secuencias de representación de Direct3D de ejemplo, con las técnicas de medición que lo acompañan. Con este conocimiento, podrá generar mediciones precisas y repetibles en llamadas individuales.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Cómo generar perfiles de una secuencia de representación de Direct3D con precisión

Ahora que se han resaltado algunos de los desafíos de generación de perfiles, en esta sección se muestran técnicas que le ayudarán a generar medidas de perfil que se pueden usar para el presupuesto. Es posible realizar mediciones de generación de perfiles precisas y repetibles si entiende la relación entre los componentes controlados por la CPU y cómo evitar las optimizaciones de rendimiento implementadas por el tiempo de ejecución y el controlador.

Para empezar, debe poder medir con precisión el tiempo de ejecución de una única llamada API.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Elija una herramienta de medición precisa como QueryPerformanceCounter

El sistema operativo Microsoft Windows incluye un temporizador de alta resolución que se puede usar para medir los tiempos transcurridos de alta resolución. El valor actual de un temporizador de este tipo se puede devolver mediante [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Después de invocar **QueryPerformanceCounter** para devolver los valores de inicio y detención, la diferencia entre los dos valores se puede convertir al tiempo real transcurrido (en segundos) mediante **QueryPerformanceCounter**.

Las ventajas de usar [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) son que está disponible en Windows y es fácil de usar. Simplemente incluya las llamadas con una llamada a **QueryPerformanceCounter** y guarde los valores de inicio y detención. Por lo tanto, en este documento se muestra cómo usar **QueryPerformanceCounter** para generar perfiles de tiempos de ejecución, de forma similar a como lo medió un generador de perfiles de instrumentación. Este es un ejemplo que muestra cómo insertar **QueryPerformanceCounter** en el código fuente:


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



Ejemplo 2: implementación de generación de perfiles personalizada con QPC

iniciar y detener son dos enteros grandes que contendrán los valores de inicio y detención devueltos por el temporizador de alto rendimiento. Observe que se llama a QueryPerformanceCounter (&Start) justo antes de que se llame a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y queryperformancecounter (&STOP) justo después de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Después de obtener el valor de detención, se llama a QueryPerformanceFrequency para devolver frec, que es la frecuencia del temporizador de alta resolución. En este ejemplo hipotético, supongamos que obtiene los siguientes resultados para Start, STOP y frec:



| Variable local | Número de TICs |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| Freq           | 3579545         |



 

Puede convertir estos valores en el número de ciclos que se tarda en ejecutar las llamadas a la API de la siguiente manera:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



En otras palabras, se tarda aproximadamente 4568 ciclos de reloj en procesar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) en este equipo de 2 GHz. Puede convertir estos valores en el tiempo real que se tardó en ejecutar todas las llamadas de la siguiente manera:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



El uso de QueryPerformanceCounter requiere que se agreguen las medidas de inicio y detención a la secuencia de representación y se use QueryPerformanceFrequency para convertir la diferencia (número de TICs) en el número de ciclos de CPU o en el tiempo real. La identificación de la técnica de medición es un buen punto de partida para desarrollar una implementación de generación de perfiles personalizada. Sin embargo, antes de empezar a crear mediciones y comenzar a realizarlas, debe saber cómo tratar con la tarjeta de vídeo.

### <a name="focus-on-cpu-measurements"></a>Centrarse en las medidas de la CPU

Como se indicó anteriormente, la CPU y la GPU funcionan en paralelo para procesar el trabajo generado por las llamadas API. Una aplicación real requiere la generación de perfiles de ambos tipos de procesadores para averiguar si la aplicación está limitada por CPU o por GPU. Dado que el rendimiento de la GPU es específico del proveedor, sería muy difícil generar resultados en este documento que cubran la variedad de tarjetas de vídeo disponibles.

En su lugar, este documento solo se centrará en la generación de perfiles del trabajo realizado por la CPU mediante una técnica personalizada para medir el tiempo de ejecución y el trabajo del controlador. El trabajo de la GPU se reducirá a una cantidad insignificante, de modo que los resultados de la CPU sean más visibles. Uno de los beneficios de este enfoque es que esta técnica produce resultados en el apéndice que debería poder correlacionar con las medidas. Para reducir el trabajo requerido por la tarjeta de vídeo a un nivel insignificante, simplemente reduzca el trabajo de representación hasta el menor importe posible. Esto puede realizarse mediante la limitación de las llamadas a Draw para representar un solo triángulo y se puede restringir aún más para que cada triángulo solo contenga un píxel.

La unidad de medida usada en este documento para medir el trabajo de CPU será el número de ciclos de reloj de la CPU en lugar de la hora real. Los ciclos de reloj de la CPU tienen la ventaja de que es más portátil (para aplicaciones limitadas por CPU) que el tiempo real transcurrido entre equipos con diferentes velocidades de CPU. Esto se puede convertir fácilmente a la hora real si se desea.

En este documento no se tratan los temas relacionados con el equilibrio de la carga de trabajo entre la CPU y la GPU. Recuerde que el objetivo de este documento es no medir el rendimiento general de una aplicación, pero para mostrarle cómo medir con precisión el tiempo que tarda el motor en tiempo de ejecución y el controlador en procesar las llamadas API. Con estas medidas precisas, puede llevar a cabo la tarea de presupuestar la CPU para comprender ciertos escenarios de rendimiento.

### <a name="controlling-runtime-and-driver-optimizations"></a>Controlar el tiempo de ejecución y las optimizaciones del controlador

Con una técnica de medición identificada y una estrategia para reducir el trabajo de GPU, el siguiente paso es conocer las optimizaciones del motor en tiempo de ejecución y los controladores que se obtienen al generar perfiles.

El trabajo de CPU se puede dividir en tres depósitos: el trabajo de la aplicación, el trabajo en tiempo de ejecución y el controlador funcionan. Omita el trabajo de la aplicación, ya que está bajo el control del programador. Desde el punto de vista de la aplicación, el tiempo de ejecución y el controlador son como casillas negras, ya que la aplicación no tiene control sobre lo que se implementa en ellos. La clave es comprender las técnicas de optimización que se pueden implementar en el tiempo de ejecución y el controlador. Si no entiende estas optimizaciones, es muy fácil pasar a la conclusión equivocada sobre la cantidad de trabajo que está haciendo la CPU en función de las medidas de perfil. En concreto, hay dos temas relacionados con algo denominado búfer de comandos y lo que puede hacer para ofuscar la generación de perfiles. Estos temas son:

-   Optimización en tiempo de ejecución con el búfer de comandos. El búfer de comandos es una optimización en tiempo de ejecución que reduce el impacto de una transición de modo. Para controlar la temporización de la transición de modo, vea [controlar el búfer de comandos](#controlling-the-command-buffer).
-   Niega los efectos de control de tiempo del búfer de comandos. El tiempo transcurrido de una transición de modo puede tener un gran impacto en las medidas de generación de perfiles. La estrategia para esto es [hacer que la secuencia de representación sea grande en comparación con la transición de modo](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Controlar el búfer de comandos

Cuando una aplicación realiza una llamada API, el tiempo de ejecución convierte la llamada de API en un formato independiente del dispositivo (que llamaremos un comando) y lo almacena en el búfer de comandos. El búfer de comandos se agrega al diagrama siguiente.

![diagrama de componentes de CPU, incluido un búfer de comandos](images/microbenchmarkcommandbuffer2.png)

Cada vez que la aplicación realiza otra llamada API, el Runtime repite esta secuencia y agrega otro comando al búfer de comandos. En algún momento, el tiempo de ejecución vacía el búfer (enviando los comandos al controlador). En Windows XP, si se vacía el búfer de comandos, se produce una transición de modo cuando el sistema operativo cambia del tiempo de ejecución (que se ejecuta en modo de usuario) al controlador (que se ejecuta en modo kernel), como se muestra en el diagrama siguiente.

-   modo de usuario: el modo de procesador sin privilegios que ejecuta el código de aplicación. Las aplicaciones de modo de usuario no pueden obtener acceso a los datos del sistema excepto a través de los servicios del sistema.
-   modo kernel: modo de procesador con privilegios en el que se ejecuta el código ejecutivo basado en Windows. Un controlador o un subproceso que se ejecuta en modo kernel tiene acceso a toda la memoria del sistema, acceso directo al hardware y las instrucciones de CPU para realizar la e/s con el hardware.

![diagrama de transiciones entre el modo de usuario y el modo kernel](images/microbenchmarkcommandbuffer3.png)

La transición se produce cada vez que la CPU cambia del modo de usuario al modo kernel (y viceversa) y el número de ciclos que requiere es grande en comparación con una llamada de API individual. Si el tiempo de ejecución envía cada llamada de API al controlador cuando se invocó, cada llamada API incurrirá en el costo de una transición de modo.

En su lugar, el búfer de comandos es una optimización en tiempo de ejecución diseñada para reducir el costo efectivo de la transición de modo. El búfer de comandos pone en cola muchos comandos de controlador para preparar una transición de modo único. Cuando el tiempo de ejecución agrega un comando al búfer de comandos, el control se devuelve a la aplicación. Un generador de perfiles no tiene ninguna manera de saber que los comandos del controlador probablemente aún no se han enviado al controlador. Como resultado, los números devueltos por un generador de perfiles de instrumentación fuera del sistema son engañosos, ya que mide el trabajo en tiempo de ejecución, pero no el trabajo del controlador asociado.

### <a name="profile-results-without-a-mode-transition"></a>Generar perfiles de resultados sin una transición de modo

Mediante el uso de la secuencia de representación del ejemplo 2, estas son algunas medidas de temporización típicas que ilustran la magnitud de una transición de modo. Suponiendo que las llamadas a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) no causan una transición de modo, un generador de perfiles de instrumentación fuera del estante podría devolver resultados similares a los siguientes:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Cada uno de estos números es la cantidad de tiempo que tarda el motor en tiempo de ejecución en agregar estas llamadas al búfer de comandos. Puesto que no hay ninguna transición de modo, el controlador no ha realizado todavía ningún trabajo. Los resultados del generador de perfiles son precisos, pero no miden todo el trabajo que la secuencia de representación hará que la CPU realice.

### <a name="profile-results-with-a-mode-transition"></a>Generar perfiles de resultados con una transición de modo

Ahora, observe lo que sucede en el mismo ejemplo cuando se produce una transición de modo. Esta vez, supongamos que [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) causan una transición de modo. Una vez más, un generador de perfiles de instrumentación fuera del estante podría devolver resultados similares a los siguientes:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



El tiempo medido para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) es aproximadamente el mismo, sin embargo, el aumento drástico en la cantidad de tiempo empleado en [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) se debe a la transición del modo. Esto es lo que sucede:

1.  Suponga que el búfer de comandos tiene espacio para un comando antes de que se inicie la secuencia de representación.
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) se convierte en un formato independiente del dispositivo y se agrega al búfer de comandos. En este escenario, esta llamada rellena el búfer de comandos.
3.  El Runtime intenta agregar [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) al búfer de comandos, pero no puede, porque está lleno. En su lugar, el tiempo de ejecución vacía el búfer de comandos. Esto provoca la transición de modo kernel. Supongamos que la transición tarda aproximadamente 5000 ciclos. Esta vez contribuye al tiempo dedicado a **DrawPrimitive**.
4.  Después, el controlador procesa el trabajo asociado a todos los comandos que se vaciaron del búfer de comandos. Suponga que el tiempo del controlador para procesar los comandos que casi rellenó el búfer del comando es de aproximadamente 935.000 ciclos. Supongamos que el trabajo del controlador asociado a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) es aproximadamente 2750 ciclos. Esta vez contribuye al tiempo dedicado a [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).
5.  Cuando el controlador finaliza su trabajo, la transición de modo de usuario devuelve el control al tiempo de ejecución. El búfer de comandos está ahora vacío. Supongamos que la transición tarda aproximadamente 5000 ciclos.
6.  La secuencia de representación finaliza mediante la conversión de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) y su adición al búfer de comandos. Suponga que esto tarda aproximadamente 900 ciclos. Esta vez contribuye al tiempo dedicado a **DrawPrimitive**.

Resumir los resultados, verá:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Al igual que la medida de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sin la transición de modo (ciclos 900), la medición de **DrawPrimitive** con la transición de modo (947.950 ciclos) es precisa pero no es útil en cuanto a la presupuestación del trabajo de CPU. El resultado contiene el trabajo correcto en tiempo de ejecución, el controlador funciona para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), el controlador funciona para los comandos que precedieron **SetTexture** y las transiciones de modo dos. Sin embargo, la medida no tiene el funcionamiento del controlador **DrawPrimitive** .

Una transición de modo podría producirse en respuesta a cualquier llamada. Depende de lo que se encontraba anteriormente en el búfer de comandos. Debe controlar la transición del modo para comprender cuánto trabajo de CPU (tiempo de ejecución y controlador) está asociado a cada llamada. Para ello, necesita un mecanismo para controlar el búfer de comandos y la temporización de la transición de modo.

### <a name="the-query-mechanism"></a>Mecanismo de consulta

El mecanismo de consulta de Microsoft Direct3D 9 se diseñó para permitir que el tiempo de ejecución consultase el progreso de la GPU y devuelva ciertos datos de la GPU. Durante la generación de perfiles, si el trabajo de la GPU está minimizado para que tenga un impacto insignificante en el rendimiento, puede devolver el estado de la GPU para ayudar a medir el trabajo del controlador. Después de todo, el trabajo del controlador se completa cuando la GPU ha detectado los comandos del controlador. Además, el mecanismo de consulta puede ser coaxial para controlar dos características de búfer de comandos importantes para la generación de perfiles: cuando el búfer de comandos se vacía y cuánto trabajo hay en el búfer.

Esta es la misma secuencia de representación mediante el mecanismo de consulta:


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



Ejemplo 3: usar una consulta para controlar el búfer de comandos

A continuación se muestra una explicación más detallada de cada una de estas líneas de código:

1.  Cree una consulta de eventos mediante la creación de un objeto de consulta con el \_ evento D3DQUERYTYPE.
2.  Agregue un marcador de evento de consulta al búfer de comandos mediante una llamada a [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ End**](d3dissue-end.md)). Este marcador indica al controlador que realice un seguimiento cuando la GPU termine de ejecutar los comandos precedidos del marcador.
3.  La primera llamada vacía el búfer de comandos porque la llamada a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con el [**\_ vaciado D3DGETDATA**](d3dgetdata-flush.md) obliga a vaciar el búfer de comandos. Cada llamada subsiguiente comprueba la GPU para ver cuándo finaliza el procesamiento de todo el trabajo de búfer de comandos. Este bucle no devuelve S \_ correcto hasta que la GPU está inactiva.
4.  Muestra la hora de inicio.
5.  Invocar las llamadas a la API que se van a perfiles.
6.  Agregue un segundo marcador de evento de consulta al búfer de comandos. Este marcador se usará para realizar el seguimiento de la finalización de las llamadas.
7.  La primera llamada vacía el búfer de comandos porque la llamada a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con el [**\_ vaciado D3DGETDATA**](d3dgetdata-flush.md) obliga a vaciar el búfer de comandos. Cuando la GPU finaliza el procesamiento de todo el trabajo de búfer de comandos, **GetData** devuelve S \_ correcto y el bucle se cierra porque la GPU está inactiva.
8.  Muestra la hora de detención.

Estos son los resultados que se miden con QueryPerformanceCounter y QueryPerformanceFrequency:



| Variable local | Número de TICs |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| Freq           | 3579545         |



 

Convertir TICs en ciclos de nuevo (en un equipo de 2 GHz):


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Este es el desglose del número de ciclos por llamada:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



El mecanismo de consulta nos ha permitido controlar el tiempo de ejecución y el trabajo de controlador que se está midiendo. Para comprender cada uno de estos números, esto es lo que sucede en respuesta a cada una de las llamadas API, junto con los tiempos estimados:

1.  La primera llamada vacía el búfer de comandos mediante una llamada a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con el [**\_ vaciado de D3DGETDATA**](d3dgetdata-flush.md). Cuando la GPU finaliza el procesamiento de todo el trabajo de búfer de comandos, **GetData** devuelve S \_ correcto y el bucle se cierra porque la GPU está inactiva.
2.  La secuencia de representación comienza por convertir [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) en un formato independiente del dispositivo y agregarlo al búfer de comandos. Suponga que esto tarda aproximadamente 100 ciclos.
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) se convierte y se agrega al búfer de comandos. Suponga que esto tarda aproximadamente 900 ciclos.
4.  [**Problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) agrega un marcador de consulta al búfer de comandos. Suponga que esto tarda aproximadamente 200 ciclos.
5.  [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) hace que el búfer de comandos se vacíe, lo que fuerza la transición del modo kernel. Suponga que esto tarda aproximadamente 5000 ciclos.
6.  A continuación, el controlador procesa el trabajo asociado a las cuatro llamadas. Supongamos que el tiempo del controlador para procesar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) es aproximadamente 2964 ciclos, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) es de aproximadamente 3600 ciclos, el [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) es de aproximadamente 200 ciclos. Por lo tanto, el tiempo total del controlador para los cuatro comandos es aproximadamente 6450 ciclos.
    > [!Note]  
    > El controlador también tarda un poco en ver cuál es el estado de la GPU. Dado que el trabajo de la GPU es trivial, la GPU ya debe realizarse. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devolverá \_ los valores correctos en función de la probabilidad de que la GPU finalice.

     

7.  Cuando el controlador finaliza su trabajo, la transición de modo de usuario devuelve el control al tiempo de ejecución. El búfer de comandos está ahora vacío. Suponga que esto tarda aproximadamente 5000 ciclos.

Los números de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) incluyen:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



El mecanismo de consulta utilizado en combinación con QueryPerformanceCounter mide todo el trabajo de la CPU. Esto se hace con una combinación de marcadores de consulta y comparaciones de estado de consulta. Los marcadores de consulta de inicio y detención agregados al búfer de comandos se utilizan para controlar la cantidad de trabajo que hay en el búfer. Si espera hasta que se devuelve el código de retorno correcto, la medida de inicio se realiza justo antes de que se inicie una secuencia de representación limpia y la medida de detención se realiza justo después de que el controlador haya finalizado el trabajo asociado con el contenido del búfer de comandos. Esto captura eficazmente el trabajo de CPU realizado por el motor en tiempo de ejecución, así como el controlador.

Ahora que conoce el búfer de comandos y el efecto que puede tener en la generación de perfiles, debe saber que hay algunas otras condiciones que pueden hacer que el tiempo de ejecución vacíe el búfer de comandos. Debe verlos en las secuencias de representación. Algunas de estas condiciones son respuesta a las llamadas a la API, mientras que otras están en respuesta a los cambios de los recursos en tiempo de ejecución. Cualquiera de las siguientes condiciones producirá una transición de modo:

-   Cuando se llama a uno de los métodos de bloqueo ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) en un búfer de vértices, un búfer de índice o una textura (bajo ciertas condiciones con ciertas marcas).
-   Cuando se crea un dispositivo o un búfer de vértices, un búfer de índice o una textura.
-   Cuando la última versión destruye un dispositivo o un búfer de vértices, un búfer de índice o una textura.
-   Cuando se llama a [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) .
-   Cuando está [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) , se llama a.
-   Cuando se llena el búfer de comandos.
-   Cuando se llama a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con el \_ vaciado de D3DGETDATA.

Tenga cuidado de ver estas condiciones en las secuencias de representación. Cada vez que se agrega una transición de modo, se agregarán 10.000 ciclos de trabajo de controlador a las medidas de generación de perfiles. Además, el búfer de comandos no tiene un tamaño estático. El tiempo de ejecución puede cambiar el tamaño del búfer en respuesta a la cantidad de trabajo que está generando la aplicación. Esta es otra optimización que depende de una secuencia de representación.

Por tanto, tenga cuidado para controlar las transiciones de modo durante la generación de perfiles. El mecanismo de consulta ofrece un método sólido para vaciar el búfer de comandos, de modo que pueda controlar la temporización de la transición de modo, así como la cantidad de trabajo que contiene el búfer. Sin embargo, incluso esta técnica se puede mejorar reduciendo el tiempo de transición de modo para que sea insignificante con respecto al resultado medido.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Hacer que la secuencia de representación sea grande en comparación con la transición de modo

En el ejemplo anterior, el modificador de modo kernel y el modificador de modo de usuario consumen aproximadamente 10.000 ciclos que no tienen nada que hacer con el tiempo de ejecución y el funcionamiento del controlador. Dado que la transición de modo se integra en el sistema operativo, no se puede reducir a cero. Para hacer que la transición de modo sea insignificante, la secuencia de representación debe ajustarse para que el trabajo de controlador y tiempo de ejecución sea un orden de magnitud mayor que los modificadores de modo. Podría intentar realizar una resta para quitar las transiciones, pero amortizar el costo en un costo de secuencia de representación mucho mayor es más confiable.

La estrategia para reducir la transición de modo hasta que se vuelve insignificante es agregar un bucle a la secuencia de representación. Por ejemplo, echemos un vistazo a los resultados de generación de perfiles si se agrega un bucle que repetirá la secuencia de presentación 1500 veces:


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



Ejemplo 4: agregar un bucle a la secuencia de representación

Estos son los resultados que se miden con QueryPerformanceCounter y QueryPerformanceFrequency:



| Variable local | Número de las marcas |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| Freq           | 3579545        |



 

El uso de QueryPerformanceCounter mide 2.840 TICs ahora. La conversión de TICs en ciclos es la misma que ya se ha mostrado:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



En otras palabras, se tarda aproximadamente 6,9 millones ciclos en esta máquina de 2 GHz en procesar las llamadas 1500 en el bucle de representación. De los ciclos 6,9 millones, la cantidad de tiempo en el modo de transición es aproximadamente de 10 000, por lo que ahora los resultados del perfil son casi totalmente medidas de trabajo asociadas a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Observe que el ejemplo de código requiere una matriz de dos texturas. Para evitar una optimización en tiempo de ejecución que quitaría [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) si establece el mismo puntero de textura cada vez que se llama, simplemente use una matriz de dos texturas. De este modo, cada vez a través del bucle, cambia el puntero de textura y se realiza el trabajo completo asociado a **SetTexture** . Asegúrese de que ambas texturas tengan el mismo tamaño y formato, de modo que ningún otro estado cambie cuando la textura sí lo sea.

Y ahora tiene una técnica para la generación de perfiles de Direct3D. Se basa en el contador de alto rendimiento (QueryPerformanceCounter) para registrar el número de pasos que tarda la CPU en procesar el trabajo. El trabajo se controla cuidadosamente para ser el tiempo de ejecución y el trabajo del controlador asociados a las llamadas de API mediante el mecanismo de consulta. Una consulta proporciona dos formas de control: primero para vaciar el búfer de comandos antes de que se inicie la secuencia de representación y, en segundo lugar, devolver cuando finalice el trabajo de la GPU.

Hasta ahora, en este documento se ha mostrado cómo generar perfiles de una secuencia de representación. Cada secuencia de representación ha sido bastante simple, lo que contiene una única llamada a [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) y una llamada a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Esto se hizo para centrarse en el búfer de comandos y el uso del mecanismo de consulta para controlarlo. A continuación se muestra un breve resumen de cómo generar perfiles de una secuencia de representación arbitraria:

-   Use un contador de alto rendimiento como QueryPerformanceCounter para medir el tiempo que se tarda en procesar cada llamada de API. Use QueryPerformanceFrequency y la tasa de reloj de la CPU para convertir esto en el número de ciclos de CPU por llamada API.
-   Minimice la cantidad de trabajo de GPU mediante la representación de listas de triángulo, donde cada triángulo contiene un píxel.
-   Use el mecanismo de consulta para vaciar el búfer de comandos antes de la secuencia de representación. Esto garantiza que la generación de perfiles capturará la cantidad correcta de tiempo de ejecución y de controlador asociado a la secuencia de representación.
-   Controlar la cantidad de trabajo que se agrega al búfer de comandos con marcadores de eventos de consulta. Esta misma consulta detecta cuándo finaliza la GPU su trabajo. Dado que el trabajo de la GPU es trivial, es prácticamente equivalente a medir Cuándo se completa el trabajo del controlador.

Todas estas técnicas se usan para generar perfiles de cambios de estado. Suponiendo que ha leído y comprendido cómo controlar el búfer de comandos y ha completado correctamente las medidas de línea base en [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), está listo para agregar cambios de estado a las secuencias de representación. Hay algunos desafíos de generación de perfiles adicionales al agregar cambios de estado a una secuencia de representación. Si desea agregar cambios de estado a las secuencias de representación, asegúrese de continuar en la sección siguiente.

## <a name="profiling-direct3d-state-changes"></a>Generar perfiles de cambios de estado de Direct3D

Direct3D usa muchos Estados de representación para controlar casi todos los aspectos de la canalización. Las API que causan cambios de estado incluyen cualquier función o método que no sea las \* llamadas primitivas Draw.

Los cambios de estado son complicados porque es posible que no pueda ver el costo de un cambio de estado sin representación. Este es el resultado del algoritmo diferido que usan el controlador y la GPU para diferir el trabajo hasta que sea absolutamente necesario. En general, debe seguir estos pasos para medir un único cambio de estado:

1.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) primero el perfil.
2.  Agregue un cambio de estado a la secuencia de representación y Perfile la nueva secuencia.
3.  Reste la diferencia entre las dos secuencias para obtener el costo del cambio de estado.

Naturalmente, todo lo que ha aprendido sobre el uso del mecanismo de consulta y la colocación de la secuencia de representación en un bucle para negar el costo de la transición de modo se sigue aplicando.

### <a name="profiling-a-simple-state-change"></a>Generar perfiles de un cambio de estado simple

A partir de una secuencia de representación que contiene [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), esta es la secuencia de código para medir el costo de agregar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



Ejemplo 5: medir una llamada API de cambio de estado

Observe que el bucle contiene dos llamadas, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). La secuencia de representación recorre el bucle 1500 veces y genera resultados similares a los siguientes:



| Variable local | Número de las marcas |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| Freq           | 3579545        |



 

La conversión de pasos a ciclos vuelve a producirse:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



La división por el número de iteraciones en el bucle produce:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Cada iteración del bucle contiene un cambio de estado y una llamada a Draw. Restar el resultado de la secuencia de representación [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) :


```
3850 - 1100 = 2750 cycles for SetTexture
```



Es el número medio de ciclos para agregar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) a esta secuencia de representación. Esta misma técnica se puede aplicar a otros cambios de estado.

¿Por qué [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) se llama un cambio de estado simple? Dado que el estado que se está configurando está restringido para que la canalización tenga la misma cantidad de trabajo cada vez que se cambia el estado. La restricción de ambas texturas al mismo tamaño y formato garantiza la misma cantidad de trabajo para cada llamada a **SetTexture** .

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Generar perfiles de un cambio de estado que se debe alternar

Hay otros cambios de estado que hacen que la cantidad de trabajo realizado por la canalización de gráficos cambie para cada iteración del bucle de representación. Por ejemplo, si está habilitada la prueba z, cada color de píxel actualiza un destino de representación solo después de que el valor z del nuevo píxel se prueba con el valor z del píxel existente. Si la prueba de z está deshabilitada, esta prueba por píxel no se realiza y la salida se escribe mucho más rápido. Al habilitar o deshabilitar el estado de la prueba z, se cambia drásticamente la cantidad de trabajo realizado (por la CPU y la GPU) durante la representación.

[**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) requiere un estado de representación determinado y un valor de estado para habilitar o deshabilitar las pruebas z. El valor de estado concreto se evalúa en tiempo de ejecución para determinar cuánto trabajo es necesario. Es difícil medir este cambio de estado en un bucle de representación y seguir condicionando el estado de la canalización para que se cambie. La única solución es alternar el cambio de estado durante la secuencia de representación.

Por ejemplo, la técnica de generación de perfiles debe repetirse dos veces como se indica a continuación:

1.  Empiece por generar perfiles de la secuencia de representación de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) . Llame a esta línea de base.
2.  Generar perfiles de una segunda secuencia de representación que alterna el cambio de estado. El bucle de la secuencia de representación contiene:
    -   Un cambio de estado para establecer el estado en una condición "false".
    -   [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) igual que la secuencia original.
    -   Un cambio de estado para establecer el estado en una condición "true".
    -   Un segundo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para forzar el segundo cambio de estado.
3.  Busque la diferencia entre las dos secuencias de representación. Para hacer esto:
    -   Multiplica la secuencia [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de línea de base por 2 porque hay dos llamadas **DrawPrimitive** en la nueva secuencia.
    -   Resta el resultado de la nueva secuencia de la secuencia original.
    -   Divida el resultado en 2 para obtener el costo medio de los cambios de estado "false" y "true".

Con la técnica de bucle utilizada en la secuencia de representación, el costo de cambiar el estado de canalización debe medirse alternando el estado de "true" a una condición "false" y viceversa, para cada iteración de la secuencia de representación. El significado de "true" y "false" aquí no son literales, esto significa simplemente que el estado debe establecerse en condiciones opuestas. Esto hace que ambos cambios de estado se midan durante la generación de perfiles. Por supuesto todo lo que ha aprendido sobre el uso del mecanismo de consulta y la colocación de la secuencia de representación en un bucle para negar el costo de la transición de modo se sigue aplicando.

Por ejemplo, esta es la secuencia de código para medir el costo de activar o desactivar las pruebas de z:


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



Ejemplo 5: medir un cambio de estado de alternancia

El bucle alterna el estado mediante la ejecución de dos llamadas a [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . La primera llamada a **SetRenderState** deshabilita las pruebas z y el segundo **SetRenderState** habilita las pruebas z. Cada **SetRenderState** va seguido de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para que el trabajo asociado con el cambio de estado lo procese el controlador en lugar de establecer solo un bit sucio en el controlador.

Estos números son razonables para esta secuencia de representación:



| Variable local | Número de TICs |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| Freq           | 3579545         |



 

La conversión de pasos a ciclos vuelve a producirse:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



La división por el número de iteraciones en el bucle produce:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Cada iteración del bucle contiene dos cambios de estado y dos llamadas a Draw. Restar las llamadas a Draw (suponiendo 1100 ciclos) deja:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Es el número medio de ciclos para ambos cambios de estado, por lo que el tiempo medio para cada cambio de estado es:


```
4000 / 2  = 2000 cycles for each state change
```



Por lo tanto, el número medio de ciclos para habilitar o deshabilitar las pruebas z es de 2000 ciclos. Merece la pena mencionar que QueryPerformanceCounter mide la mitad del tiempo y la mitad del tiempo deshabilitada para z. Esta técnica mide realmente el promedio de ambos cambios de estado. En otras palabras, está midiendo el tiempo para alternar un estado. Con esta técnica, no tiene ninguna manera de saber si los tiempos de habilitación y deshabilitación son equivalentes, ya que ha medido el promedio de ambos. No obstante, se trata de un número razonable que se usa al presupuestar un estado de alternancia como una aplicación que hace que este cambio de estado solo pueda hacerlo alternando este estado.

Por lo tanto, ahora puede aplicar estas técnicas y generar perfiles de todos los cambios de estado que desee, ¿es correcto? No del todo. Todavía tiene que tener cuidado con las optimizaciones que están diseñadas para reducir la cantidad de trabajo que debe realizarse. Hay dos tipos de optimizaciones que se deben tener en cuenta al diseñar las secuencias de representación.

### <a name="watch-out-for-state-change-optimizations"></a>Ver las optimizaciones de cambio de estado

En la sección anterior se muestra cómo generar perfiles de ambos tipos de cambios de estado: un cambio de estado simple que está restringido para generar la misma cantidad de trabajo para cada iteración y un cambio de estado de alternancia que cambia drásticamente la cantidad de trabajo realizada. ¿Qué ocurre si toma la secuencia de representación anterior y agrega otro cambio de estado a ella? Por ejemplo, en este ejemplo se toma la secuencia de representación z>-enable y se le agrega una comparación entre z-FUNC:


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



El estado z-FUNC establece el nivel de comparación al escribir en el búfer z (entre el valor z de un píxel actual con el valor z de un píxel en el búfer de profundidad). D3DCMP \_ nunca desactiva la comparación de pruebas z mientras que D3DCMP \_ siempre establece la comparación para que suceda cada vez que se realiza la prueba z.

La generación de perfiles de uno de estos cambios de estado en una secuencia de representación con [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) genera resultados similares a los siguientes:



| Cambio de estado único | Número promedio de ciclos |
|---------------------|--------------------------|
| \_Solo D3DRS ZENABLE | 2000                     |



 

or



| Cambio de estado único | Número promedio de ciclos |
|---------------------|--------------------------|
| \_Solo D3DRS ZFUNC   | 600                      |



 

Sin embargo, si \_ genera el perfil de D3DRS ZENABLE y D3DRS \_ ZFUNC en la misma secuencia de representación, podría ver resultados como los siguientes:



| Ambos cambios de estado            | Número promedio de ciclos |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRS \_ ZFUNC | 2000                     |



 

Podría esperar que el resultado sea la suma de los ciclos 2000 y 600 (o 2600) porque el controlador está realizando todo el trabajo asociado a la configuración de ambos Estados de representación. En su lugar, el promedio es 2000 ciclos.

Este resultado refleja una optimización de cambio de estado implementada en el tiempo de ejecución, el controlador o la GPU. En este caso, el controlador podría ver la primera [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y establecer un estado sucio que pospuso el trabajo hasta más tarde. Cuando el controlador Ve el segundo **SetRenderState**, el mismo estado modificado podría estar establecido de redundancia y el mismo trabajo se pospuso una vez más. Cuando se llama a [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , el trabajo asociado con el estado Dirty se procesa finalmente. El controlador ejecuta el trabajo una vez, lo que significa que el controlador consolida en efecto los dos primeros cambios de estado. De forma similar, el controlador consolida el tercer y cuarto cambio de estado de forma eficaz en un solo cambio de estado cuando se llama al segundo **DrawPrimitive** . El resultado neto es que el controlador y la GPU procesan un solo cambio de estado para cada llamada a Draw.

Este es un buen ejemplo de optimización de un controlador dependiente de la secuencia. El controlador pospuso el trabajo dos veces estableciendo un estado modificado y, a continuación, realizó el trabajo una vez para borrar el estado sucio. Este es un buen ejemplo del tipo de mejora de la eficacia que puede tener lugar cuando se aplaza el trabajo hasta que sea absolutamente necesario.

¿Cómo se sabe qué cambios de estado establecen un estado modificado internamente y, por tanto, se pospone el trabajo hasta más tarde? Solo mediante la prueba de secuencias de representación (o la comunicación con los escritores de controladores). Los controladores se actualizan y mejoran periódicamente para que la lista de optimizaciones no sea estática. Solo hay una manera de saber absolutamente cuál es el costo de un cambio de estado en una secuencia de representación determinada, en un conjunto de hardware determinado. y eso es medirlo.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Ver las optimizaciones de DrawPrimitive

Además de las optimizaciones de cambio de estado, el tiempo de ejecución intentará optimizar el número de llamadas a Draw que el controlador tiene que procesar. Por ejemplo, tenga en cuenta estas llamadas de vuelta a Draw:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Ejemplo 5A: dos llamadas a Draw

Esta secuencia contiene dos llamadas a Draw, que el Runtime consolidará en una única llamada equivalente a:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Ejemplo 5B: una única llamada a Draw concatenada

El tiempo de ejecución concatenará ambas llamadas a Draw en una sola llamada, lo que reduce el trabajo del controlador en un 50 por ciento, ya que el controlador ahora solo necesitará procesar una llamada a Draw.

En general, el motor en tiempo de ejecución concatenará dos o más llamadas [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de vuelta a la inversa cuando:

1.  El tipo primitivo es una lista de triángulos (D3DPT \_ TRIANGLELIST).
2.  Cada llamada [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sucesiva debe hacer referencia a vértices consecutivos en el búfer de vértices.

Del mismo modo, las condiciones adecuadas para concatenar dos o más llamadas de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) de retroceso son:

1.  El tipo primitivo es una lista de triángulos (D3DPT \_ TRIANGLELIST).
2.  Cada llamada [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) sucesiva debe hacer referencia secuencial de índices consecutivos en el búfer de índice.
3.  Cada llamada [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) sucesiva debe usar el mismo valor para BaseVertexIndex.

Para evitar la concatenación durante la generación de perfiles, modifique la secuencia de representación de modo que el tipo primitivo no sea una lista de triángulos o modifique la secuencia de representación para que no haya ninguna llamada de dibujo de vuelta atrás que use vértices consecutivos (o índices). Más concretamente, el tiempo de ejecución también concatenará las llamadas a Draw que cumplan las dos condiciones siguientes:

-   Cuando la llamada anterior es [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), si la siguiente llamada a Draw:
    -   usa una lista de triángulos y
    -   especifica StartVertex = anterior StartVertex + PrimitiveCount anterior \* 3
-   Cuando se usa [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), si la siguiente llamada a Draw:
    -   usa una lista de triángulos y
    -   especifica StartIndex = anterior StartIndex + PrimitiveCount anterior \* 3 y
    -   especifica BaseVertexIndex = BaseVertexIndex anterior

Este es un ejemplo más sutil de concatenación de llamadas a Draw que es fácil de pasar por alto cuando se generan perfiles. Supongamos que la secuencia de representación tiene el siguiente aspecto:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Ejemplo 5C: un cambio de estado y una llamada a Draw

El bucle recorre en iteración hasta 1500 triángulos, estableciendo una textura y dibujando cada triángulo. Este bucle de representación tarda aproximadamente 2750 ciclos en los ciclos [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y 1100 de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) como se muestra en las secciones anteriores. Podría esperar de forma intuitiva que mover **SetTexture** fuera del bucle de representación debe reducir la cantidad de trabajo realizado por el controlador en 1500 \* 2750 ciclos, que es la cantidad de trabajo asociada a la llamada a **SetTexture** 1500 veces. El fragmento de código tendría el siguiente aspecto:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Ejemplo 5D: ejemplo 5C con el cambio de estado fuera del bucle

Mover [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) fuera del bucle de representación reduce la cantidad de trabajo asociado a **SetTexture** , ya que se llama una vez en lugar de 1500 veces. Un efecto secundario menos obvio es que el trabajo de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) también se reduce de 1500 llamadas a 1 llamada porque se cumplen todas las condiciones para concatenar llamadas a Draw. Cuando se procesa la secuencia de representación, el tiempo de ejecución procesará las llamadas 1500 en una única llamada de controlador. Al mover esta línea de código, la cantidad de trabajo del controlador se ha reducido drásticamente:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Estos resultados son completamente correctos, pero son muy engañosos en el contexto de la pregunta original. La optimización de llamadas de Draw ha provocado que la cantidad de trabajo de controlador se reduzca drásticamente. Se trata de un problema común al realizar la generación de perfiles personalizada. Al eliminar llamadas de una secuencia de representación, tenga cuidado de evitar la concatenación de llamadas a Draw. De hecho, este escenario es un eficaz ejemplo de la cantidad de mejoras en el rendimiento del controlador posible gracias a esta optimización en tiempo de ejecución.

Ahora ya sabe cómo medir los cambios de estado. Empiece por generar perfiles de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). A continuación, agregue cada cambio de estado adicional a la secuencia (en algunos casos, agregando una llamada y en otros casos agregando dos llamadas) y mide la diferencia entre las dos secuencias. Puede convertir los resultados en pasos o ciclos u hora. Al igual que la medición de secuencias de representación con QueryPerformanceCounter, la medida de los cambios de estado individuales se basa en el mecanismo de consulta para controlar el búfer de comandos y en un bucle para minimizar el impacto de las transiciones de modo. Esta técnica mide el costo de alternar un estado, ya que el generador de perfiles devuelve el promedio de habilitar y deshabilitar el estado.

Con esta capacidad, puede empezar a generar secuencias de representación arbitrarias y a medir con precisión el tiempo de ejecución y el trabajo del controlador asociados. A continuación, se pueden usar los números para responder a las preguntas de la cotización, como "el número de llamadas más que se pueden realizar" en la secuencia de representación, a la vez que se mantiene una velocidad de fotogramas razonable, suponiendo escenarios limitados por la CPU.

## <a name="summary"></a>Resumen

En este documento se muestra cómo controlar el búfer de comandos para que se puedan crear perfiles de forma precisa de las llamadas individuales. Los números de generación de perfiles se pueden generar en pasos, ciclos o en tiempo absoluto. Representan la cantidad de trabajo de controlador y tiempo de ejecución asociado a cada llamada de API.

Empiece por generar perfiles de una \* llamada primitiva Draw en una secuencia de representación. Recuerde:

1.  Use QueryPerformanceCounter para medir el número de TICs por llamada API. Use QueryPerformanceFrequency para convertir los resultados en ciclos u hora si lo desea.
2.  Use el mecanismo de consulta para vaciar el búfer de comandos antes de iniciarse.
3.  Incluya la secuencia de representación en un bucle para minimizar el impacto de la transición de modo.
4.  Use el mecanismo de consulta para medir el momento en que la GPU ha completado su trabajo.
5.  Vea la concatenación en tiempo de ejecución que tendrá un impacto importante en la cantidad de trabajo realizado.

Esto le proporciona un rendimiento básico para [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) que se puede usar para compilar desde. Para generar perfiles de un cambio de estado, siga estas sugerencias adicionales:

1.  Agregue el cambio de estado a una secuencia de representación conocida Perfil de la nueva secuencia. Dado que las pruebas se realizan en un bucle, esto requiere establecer el estado dos veces en valores opuestos (como habilitar y deshabilitar por ejemplo).
2.  Compare la diferencia en los tiempos de ciclo entre las dos secuencias.
3.  En el caso de los cambios de estado que cambian significativamente la canalización (como [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), reste la diferencia entre las dos secuencias para obtener la hora de cambio de estado.
4.  En el caso de los cambios de estado que cambian significativamente la canalización (y, por consiguiente, requieren Estados de alternancia como [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)), reste la diferencia entre las secuencias de representación y divida por 2. Esto generará el promedio de ciclos para cada cambio de estado.

Pero tenga cuidado con las optimizaciones que causan resultados inesperados durante la generación de perfiles. Las optimizaciones de cambio de estado pueden establecer Estados modificados que provocan que se difiera el trabajo. Esto puede producir resultados de perfil que no son tan intuitivos como se espera. Las llamadas a Draw que se concatenan reducirán drásticamente el trabajo del controlador, lo que puede dar lugar a conclusiones engañosas. Las secuencias de representación planeadas cuidadosamente se usan para impedir que se produzcan los cambios de estado y las concatenaciones de llamadas a Draw. El truco es evitar que las optimizaciones se produzcan durante la generación de perfiles, de modo que los números que genere sean números de presupuesto razonables.

> [!Note]  
> La duplicación de esta estrategia de generación de perfiles en una aplicación sin el mecanismo de consulta es más difícil. Antes de Direct3D 9, la única manera predecible de vaciar el búfer de comandos es bloquear una superficie activa (como un destino de representación) para esperar hasta que la GPU esté inactiva. Esto se debe a que el bloqueo de una superficie obliga al tiempo de ejecución a vaciar el búfer de comandos en caso de que haya algún comando de representación en el búfer que deba actualizar la superficie antes de que se bloquee, además de esperar a que la GPU finalice. Esta técnica es funcional, aunque es más molesta que usar el mecanismo de consulta incluido en Direct3D 9.

 

## <a name="appendix"></a>Apéndice

Los números de esta tabla son una serie de aproximaciones para la cantidad de trabajo de controlador y en tiempo de ejecución asociado a cada uno de estos cambios de estado. Las aproximaciones se basan en las medidas reales realizadas en los controladores mediante las técnicas que se muestran en el documento. Estos números se generaron mediante el tiempo de ejecución de Direct3D 9 y dependen del controlador.

Las técnicas de este documento están diseñadas para medir el funcionamiento del tiempo de ejecución y del controlador. En general, no es práctico proporcionar resultados que coincidan con el rendimiento de la CPU y la GPU en todas las aplicaciones, ya que esto requeriría una matriz exhaustiva de secuencias de representación. Además, es especialmente difícil el rendimiento de las pruebas comparativas de la GPU, ya que depende en gran medida de la configuración de estado de la canalización antes de la secuencia de representación. Por ejemplo, la habilitación de la combinación alfa no afecta a la cantidad de trabajo necesario para la CPU, pero puede tener un gran impacto en la cantidad de trabajo realizado por la GPU. Por lo tanto, las técnicas de este documento restringen el trabajo de la GPU a la cantidad mínima posible limitando la cantidad de datos que se deben representar. Esto significa que los números de la tabla coincidirán más estrechamente con los resultados obtenidos de las aplicaciones limitadas por la CPU (en lugar de a una aplicación limitada por la GPU).

Se recomienda usar las técnicas que se presentan para cubrir los escenarios y configuraciones más importantes para usted. Los valores de la tabla se pueden utilizar para comparar con los números que genera. Puesto que cada controlador varía, la única manera de generar los números reales que verá es generar resultados de generación de perfiles con los escenarios.



| Llamada a la API                             | Número promedio de ciclos |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500-11250             |
| SetFVF                               | 6400-11200             |
| SetVertexShader                      | 3000-12100             |
| SetPixelShader                       | 6300-7000              |
| SPECULARENABLE                       | 1900-11200             |
| SetRenderTarget                      | 6000-6250              |
| SetPixelShaderConstant (1 constante)  | 1500-9000              |
| NORMALIZENORMALS                     | 2200-8100              |
| LightEnable                          | 1300-9000              |
| SetStreamSource                      | 3700-5800              |
| ILUMINACIÓN                             | 1700-7500              |
| DIFFUSEMATERIALSOURCE                | 900-8300               |
| AMBIENTMATERIALSOURCE                | 900-8200               |
| COLORVERTEX                          | 800-7800               |
| SetLight                             | 2200-5100              |
| SetTransform                         | 3200-3750              |
| SetIndices                           | 900-5600               |
| AMBIENTES                              | 1150-4800              |
| SetTexture                           | 2500-3100              |
| SPECULARMATERIALSOURCE               | 900-4600               |
| EMISSIVEMATERIALSOURCE               | 900-4500               |
| SetMaterial                          | 1000-3700              |
| ZENABLE                              | 700-3900               |
| WRAP0                                | 1600-2700              |
| MINFILTER                            | 1700-2500              |
| MAGFILTER                            | 1700-2400              |
| SetVertexShaderConstant (1 constante) | 1000-2700              |
| COLOROP                              | 1500-2100              |
| COLORARG2                            | 1300-2000              |
| COLORARG1                            | 1300-1980              |
| CULLMODE                             | 500-2570               |
| SALTE                             | 500-2550               |
| DrawIndexedPrimitive                 | 1200-1400              |
| ADDRESSV                             | 1090-1500              |
| ADDRESSU                             | 1070-1500              |
| DrawPrimitive                        | 1050-1150              |
| SRGBTEXTURE                          | 150-1500               |
| STENCILMASK                          | 570-700                |
| STENCILZFAIL                         | 500-800                |
| STENCILREF                           | 550-700                |
| ALPHABLENDENABLE                     | 550-700                |
| STENCILFUNC                          | 560-680                |
| STENCILWRITEMASK                     | 520-700                |
| STENCILFAIL                          | 500-750                |
| ZFUNC                                | 510-700                |
| ZWRITEENABLE                         | 520-680                |
| STENCILENABLE                        | 540-650                |
| STENCILPASS                          | 560-630                |
| SRCBLEND                             | 500-685                |
| Dos \_ \_ StencilMODE              | 450-590                |
| ALPHATESTENABLE                      | 470-525                |
| ALPHAREF                             | 460-530                |
| ALPHAFUNC                            | 450-540                |
| DESTBLEND                            | 475-510                |
| COLORWRITEENABLE                     | 465-515                |
| CCW \_ STENCILFAIL                     | 340-560                |
| CCW \_ STENCILPASS                     | 340-545                |
| CCW \_ STENCILZFAIL                    | 330-495                |
| SCISSORTESTENABLE                    | 375-440                |
| CCW \_ STENCILFUNC                     | 250-480                |
| SetScissorRect                       | 150-340                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 
