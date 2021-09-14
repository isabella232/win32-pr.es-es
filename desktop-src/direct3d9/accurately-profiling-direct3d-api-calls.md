---
description: Una vez que tenga una aplicación de Microsoft Direct3D funcional y desee mejorar su rendimiento, generalmente usará una herramienta de generación de perfiles estándar o alguna técnica de medición personalizada para medir el tiempo necesario para ejecutar una o varias llamadas a la interfaz de programación de aplicaciones (API). Si ha hecho esto pero está obteniendo resultados de tiempo que varían de una secuencia de representación a la siguiente, o está realizando hipótesis que no se mantienen hasta los resultados reales del experimento, la siguiente información puede ayudarle a entender por qué.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Generación precisa de perfiles de llamadas de la API de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb6d60fcc1b3ace4112dbf7028d91e2c9c8b345
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060796"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Generación precisa de perfiles de llamadas de la API de Direct3D (Direct3D 9)

-   [La generación de perfiles precisa de Direct3D es difícil](#accurately-profiling-direct3d-is-difficult)
-   [Cómo crear perfiles precisos de una secuencia de representación de Direct3D](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Generar perfiles de cambios de estado de Direct3D](#profiling-direct3d-state-changes)
-   [Resumen](#summary)
-   [Apéndice](#appendix)

Una vez que tenga una aplicación de Microsoft Direct3D funcional y desee mejorar su rendimiento, generalmente usará una herramienta de generación de perfiles estándar o alguna técnica de medición personalizada para medir el tiempo necesario para ejecutar una o varias llamadas a la interfaz de programación de aplicaciones (API). Si ha hecho esto pero está obteniendo resultados de tiempo que varían de una secuencia de representación a la siguiente, o está realizando hipótesis que no se mantienen hasta los resultados reales del experimento, la siguiente información puede ayudarle a entender por qué.

La información proporcionada aquí se basa en la suposición de que tiene conocimientos y experiencia con lo siguiente:

-   Programación de C/C++
-   Programación de la API de Direct3D
-   Medición del tiempo de API
-   La tarjeta de vídeo y su controlador de software
-   Posibles resultados inexplicables de la experiencia de generación de perfiles anterior

## <a name="accurately-profiling-direct3d-is-difficult"></a>La generación de perfiles precisa de Direct3D es difícil

Un profiler informa sobre la cantidad de tiempo empleado en cada llamada API. Esto se hace para mejorar el rendimiento mediante la búsqueda y el ajuste de las zonas de acceso más populares. Hay diferentes tipos de generadores de perfiles y técnicas de generación de perfiles.

-   Un profiler de muestreo se queda inactivo la mayor parte del tiempo, lo que hace que, a intervalos específicos, muestree (o registre) las funciones que se ejecutan. Devuelve el porcentaje de tiempo empleado en cada llamada. Por lo general, un profiler de muestreo no es muy invasivo para la aplicación y tiene un impacto mínimo en la sobrecarga de la aplicación.
-   Un profiler de instrumentación mide el tiempo real que se tarda en devolver una llamada. Requiere compilar delimitadores start y stop en una aplicación. Un profiler de instrumentación es comparativamente más invasivo para una aplicación que un profiler de muestreo.
-   También es posible usar una técnica de generación de perfiles personalizada con un temporizador de alto rendimiento. Esto genera resultados muy similares a los de un generador de perfiles de instrumentación.

El tipo de generador de perfiles o la técnica de generación de perfiles que se usa solo forma parte del desafío de generar medidas precisas.

La generación de perfiles proporciona respuestas que le ayudan a presupuestar el rendimiento. Por ejemplo, supongamos que sabe que una llamada API promedia mil ciclos de reloj para ejecutarse. Puede afirmar algunas conclusiones sobre el rendimiento, como las siguientes:

-   Una CPU de 2 GHz (que dedica el 50 % de su representación de tiempo) se limita a llamar a esta API 1 millón de veces por segundo.
-   Para lograr 30 fotogramas por segundo, no puede llamar a esta API más de 33 000 veces por fotograma.
-   Solo puede representar 3,3 000 objetos por fotograma (suponiendo que 10 de estas llamadas API para la secuencia de representación de cada objeto).

En otras palabras, si tuviera tiempo suficiente por llamada API, podría responder a una pregunta de presupuestos, como el número de primitivas que se pueden representar de forma interactiva. Pero los números sin procesar devueltos por un profiler instrumentador no responderán con precisión a las preguntas de presupuesto. Esto se debe a que la canalización de gráficos tiene problemas de diseño complejos, como el número de componentes que deben funcionar, el número de procesadores que controlan cómo fluye el trabajo entre los componentes y las estrategias de optimización implementadas en el tiempo de ejecución y en un controlador que están diseñados para que la canalización sea más eficaz.

### <a name="each-api-call-goes-through-several-components"></a>Cada llamada API pasa por varios componentes

Varios componentes procesan cada llamada en su camino desde la aplicación a la tarjeta de vídeo. Por ejemplo, considere la siguiente secuencia de representación que contiene dos llamadas para dibujar un triángulo único:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



En el siguiente diagrama conceptual se muestran los distintos componentes por los que deben pasar las llamadas.

![diagrama de componentes gráficos por los que se llama a la API](images/microbenchmarkinstructionflow2.png)

La aplicación invoca Direct3D, que controla la escena, controla las interacciones del usuario y determina cómo se realiza la representación. Todo este trabajo se especifica en la secuencia de representación, que se envía al tiempo de ejecución mediante llamadas a la API de Direct3D. La secuencia de representación es virtualmente independiente del hardware (es decir, las llamadas API son independientes del hardware, pero una aplicación tiene conocimiento de las características que admite una tarjeta de vídeo).

El tiempo de ejecución convierte estas llamadas en un formato independiente del dispositivo. El tiempo de ejecución controla toda la comunicación entre la aplicación y el controlador, de modo que una aplicación se ejecutará en más de un fragmento de hardware compatible (en función de las características necesarias). Al medir una llamada de función, un profiler de instrumentación mide el tiempo empleado en una función, así como el tiempo que la función debe devolver. Una limitación de un profiler de instrumentación es que puede no incluir el tiempo que tarda un controlador en enviar el trabajo resultante a la tarjeta de vídeo ni el tiempo para que la tarjeta de vídeo procese el trabajo. En otras palabras, un generador de perfiles de instrumentación no puede atribuir todo el trabajo asociado a cada llamada de función.

El controlador de software usa conocimientos específicos de hardware sobre la tarjeta de vídeo para convertir los comandos independientes del dispositivo en una secuencia de comandos de tarjeta de vídeo. Los controladores también pueden optimizar la secuencia de comandos que se envían a la tarjeta de vídeo, de modo que la representación en la tarjeta de vídeo se realiza de forma eficaz. Estas optimizaciones pueden causar problemas de generación de perfiles porque la cantidad de trabajo realizado no es la que parece ser (es posible que tenga que comprender las optimizaciones para tenerlas en cuenta). Normalmente, el controlador devuelve el control al tiempo de ejecución antes de que la tarjeta de vídeo haya terminado de procesar todos los comandos.

La tarjeta de vídeo realiza la mayor parte de la representación mediante la combinación de datos de los búferes de vértice e índice, texturas, información de estado de representación y los comandos de gráficos. Cuando finaliza la representación de la tarjeta de vídeo, se completa el trabajo creado a partir de la secuencia de representación.

Cada componente debe procesar cada llamada a la API de Direct3D (el tiempo de ejecución, el controlador y la tarjeta de vídeo) para representar cualquier cosa.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Hay más de un procesador que controla los componentes

La relación entre estos componentes es aún más compleja, ya que la aplicación, el tiempo de ejecución y el controlador se controlan mediante un procesador y la tarjeta de vídeo se controla mediante un procesador independiente. En el diagrama siguiente se muestran dos tipos de procesadores: una unidad de procesamiento central (CPU) y una unidad de procesamiento gráfico (GPU).

![diagrama de una CPU y una GPU y sus componentes](images/microbenchmarkprocessors.png)

Los sistemas de PC tienen al menos una CPU y una GPU, pero pueden tener más de una o ambas. Las CPU se encuentran en la placa base y las GPU se encuentran en la placa base o en la tarjeta de vídeo. La velocidad de la CPU viene determinada por un chip de reloj en la placa base y la velocidad de la GPU viene determinada por un chip de reloj independiente. El reloj de CPU controla la velocidad del trabajo realizado por la aplicación, el tiempo de ejecución y el controlador. La aplicación envía trabajo a la GPU a través del entorno de ejecución y el controlador.

La CPU y la GPU suelen ejecutarse a velocidades diferentes, independientemente de las otras. La GPU puede responder al trabajo en cuanto el trabajo esté disponible (suponiendo que la GPU haya terminado de procesar el trabajo anterior). El trabajo de GPU se realiza en paralelo con el trabajo de CPU, tal y como se resalta en la línea curva de la ilustración anterior. Por lo general, un profiler mide el rendimiento de la CPU, no la GPU. Esto dificulta la generación de perfiles, ya que las medidas realizadas por un generador de perfiles de instrumentación incluyen el tiempo de CPU, pero puede que no incluyan el tiempo de GPU.

El propósito de la GPU es desactivar el procesamiento de carga desde la CPU a un procesador diseñado específicamente para el trabajo de gráficos. En las tarjetas de vídeo modernas, la GPU reemplaza gran parte del trabajo de transformación e iluminación en la canalización desde la CPU a la GPU. Esto reduce considerablemente la carga de trabajo de CPU, lo que deja más ciclos de CPU disponibles para otro procesamiento. Para optimizar una aplicación gráfica para obtener un rendimiento máximo, debe medir el rendimiento de la CPU y la GPU, y equilibrar el trabajo entre los dos tipos de procesadores.

En este documento no se tratan temas relacionados con la medición del rendimiento de la GPU ni el equilibrio del trabajo entre la CPU y la GPU. Si desea comprender mejor el rendimiento de una GPU (o una tarjeta de vídeo determinada), visite el sitio web del proveedor para buscar más información sobre el rendimiento de GPU. En su lugar, este documento se centra en el trabajo realizado por el tiempo de ejecución y el controlador al reducir el trabajo de GPU a una cantidad insignificante. Esto se basa, en parte, en la experiencia de que las aplicaciones que experimentan problemas de rendimiento suelen tener limitaciones de CPU.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Las optimizaciones de tiempo de ejecución y controlador pueden enmascarar las medidas de API

El tiempo de ejecución tiene una optimización del rendimiento integrada que puede sobrecargar la medición de una llamada individual. Este es un escenario de ejemplo que muestra este problema. Considere la siguiente secuencia de representación:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Ejemplo 1: Secuencia de representación simple

Si observa los resultados de las dos llamadas en la secuencia de representación, un profiler de instrumentación podría devolver resultados similares a estos:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



El profiler devuelve el número de ciclos de CPU necesarios para procesar el trabajo asociado a cada llamada (recuerde que la GPU no está incluida en estos números porque la GPU todavía no ha empezado a trabajar en estos comandos). Dado [**que IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) requería casi un millón de ciclos para procesar, podría concluir que no es muy eficaz. Sin embargo, pronto verá por qué esta conclusión es incorrecta y cómo puede generar resultados que se pueden usar para la presupuestación.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>La medición de los cambios de estado requiere secuencias de representación cuidadosas

Todas las llamadas que no son [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)o [**Clear**](/windows/desktop/api) (como [**SetTexture,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**SetVertexDeclaration**](/windows/desktop/api)y [**SetRenderState)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)producen un cambio de estado. Cada cambio de estado establece el estado de canalización que controla cómo se realizará la representación.

Las optimizaciones en tiempo de ejecución o el controlador están diseñadas para acelerar la representación reduciendo la cantidad de trabajo necesario. A continuación se muestra un par de optimizaciones de cambios de estado que pueden causar promedios de perfil:

-   Un controlador (o el tiempo de ejecución) podría guardar un cambio de estado como un estado local. Dado que el controlador podría funcionar en un algoritmo "diferido" (posponer el trabajo hasta que sea absolutamente necesario), el trabajo asociado a algunos cambios de estado podría retrasarse.
-   El tiempo de ejecución (o un controlador) puede quitar los cambios de estado mediante la optimización. Un ejemplo de esto podría ser quitar un cambio de estado redundante que deshabilite la iluminación porque la iluminación se ha deshabilitado previamente.

No hay ninguna manera infalible de ver una secuencia de representación y concluir qué cambios de estado establecerán un bit desaplazado y aplazarán el trabajo, o simplemente se quitarán mediante la optimización. Aunque pueda identificar cambios de estado optimizados en el tiempo de ejecución o el controlador de hoy, es probable que el entorno de ejecución o el controlador de mañana se actualicen. Tampoco sabe fácilmente cuál era el estado anterior, por lo que es difícil identificar cambios de estado redundantes. La única manera de comprobar el costo de un cambio de estado es medir la secuencia de representación que incluye los cambios de estado.

Como puede ver, las complicaciones causadas por tener varios procesadores, los comandos que procesa más de un componente y las optimizaciones integradas en los componentes dificultan la predicción de la generación de perfiles. En la sección siguiente, se abordará cada uno de estos desafíos de generación de perfiles. Se mostrarán secuencias de representación de Direct3D de ejemplo, con las técnicas de medición que lo acompañan. Con este conocimiento, podrá generar medidas precisas y repetibles en llamadas individuales.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Cómo crear perfiles precisos de una secuencia de representación de Direct3D

Ahora que se han resaltado algunos de los desafíos de generación de perfiles, en esta sección se mostrarán técnicas que le ayudarán a generar medidas de perfil que se pueden usar para la generación de presupuestos. Las medidas de generación de perfiles precisas y repetibles son posibles si comprende la relación entre los componentes controlados por la CPU y cómo evitar las optimizaciones de rendimiento implementadas por el motor en tiempo de ejecución y el controlador.

Para comenzar, debe poder medir con precisión el tiempo de ejecución de una sola llamada API.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Selección de una herramienta de medida precisa como QueryPerformanceCounter

El sistema Windows microsoft incluye un temporizador de alta resolución que se puede usar para medir los tiempos transcurridos de alta resolución. El valor actual de uno de estos temporizadores se puede devolver [**mediante QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Después de invocar **QueryPerformanceCounter** para devolver valores de inicio y de detenerse, la diferencia entre los dos valores se puede convertir al tiempo transcurrido real (en segundos) mediante **QueryPerformanceCounter**.

Las ventajas de usar [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) son que está disponible en Windows y es fácil de usar. Basta con rodear las llamadas con **una llamada a QueryPerformanceCounter** y guardar los valores de inicio y de detenerse. Por lo tanto, en este documento se muestra cómo usar **QueryPerformanceCounter** para crear perfiles de tiempos de ejecución, de forma similar a como lo mediría un generador de perfiles instrumentador. Este es un ejemplo que muestra cómo insertar **QueryPerformanceCounter en** el código fuente:


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



Ejemplo 2: Implementación de generación de perfiles personalizada con QPC

start y stop son dos enteros grandes que contendrán los valores start y stop devueltos por el temporizador de alto rendimiento. Observe que se llama a QueryPerformanceCounter(&start) justo antes de llamar a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y QueryPerformanceCounter(&stop) justo después de [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Después de obtener el valor stop, se llama a QueryPerformanceFrequency para devolver freq, que es la frecuencia del temporizador de alta resolución. En este ejemplo hipotético, supongamos que obtiene los siguientes resultados para start, stop y freq:



| Variable local | Número de pasos |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| Freq           | 3579545         |



 

Puede convertir estos valores en el número de ciclos que se tardan en ejecutar las llamadas API de la siguiente forma:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



En otras palabras, se tardan unos 4568 ciclos de reloj en procesar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) en esta máquina de 2 GHz. Puede convertir estos valores en el tiempo real que tardó en ejecutar todas las llamadas de esta forma:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



El uso de QueryPerformanceCounter requiere que agregue medidas de inicio y de detenerse a la secuencia de representación y use QueryPerformanceFrequency para convertir la diferencia (número de tics) en el número de ciclos de CPU o en tiempo real. Identificar la técnica de medición es un buen inicio para desarrollar una implementación de generación de perfiles personalizada. Pero antes de empezar a realizar medidas, debe saber cómo tratar con la tarjeta de vídeo.

### <a name="focus-on-cpu-measurements"></a>Centrarse en las medidas de CPU

Como se indicó anteriormente, la CPU y la GPU funcionan en paralelo para procesar el trabajo generado por las llamadas API. Una aplicación real requiere la generación de perfiles de ambos tipos de procesadores para averiguar si la aplicación está limitada por CPU o por GPU. Dado que el rendimiento de GPU es específico del proveedor, sería muy difícil generar resultados en este documento que cubren la variedad de tarjetas de vídeo disponibles.

En su lugar, este documento se centrará únicamente en la generación de perfiles del trabajo realizado por la CPU mediante una técnica personalizada para medir el tiempo de ejecución y el trabajo del controlador. El trabajo de GPU se reducirá a una cantidad insignificante, de modo que los resultados de la CPU sean más visibles. Una ventaja de este enfoque es que esta técnica produce resultados en el Apéndice que debería poder correlacionar con las medidas. Para reducir el trabajo que requiere la tarjeta de vídeo a un nivel insignificante, basta con reducir el trabajo de representación a la menor cantidad posible. Esto se puede lograr limitando las llamadas a draw para representar un único triángulo y se puede restringir aún más para que cada triángulo solo contenga un píxel.

La unidad de medida usada en este documento para medir el trabajo de CPU será el número de ciclos de reloj de CPU en lugar de la hora real. Los ciclos de reloj de CPU tienen la ventaja de que son más portátiles (para aplicaciones con cpu limitada) que el tiempo real transcurrido entre máquinas con diferentes velocidades de CPU. Esto se puede convertir fácilmente a la hora real si lo desea.

En este documento no se tratan temas relacionados con el equilibrio de la carga de trabajo entre la CPU y la GPU. Recuerde que el objetivo de este documento no es medir el rendimiento general de una aplicación, sino mostrar cómo medir con precisión el tiempo que tardan el tiempo en tiempo de ejecución y el controlador para procesar las llamadas API. Con estas medidas precisas, puede asumir la tarea de presupuestar la CPU para comprender determinados escenarios de rendimiento.

### <a name="controlling-runtime-and-driver-optimizations"></a>Controlar las optimizaciones de tiempo de ejecución y controladores

Con una técnica de medición identificada y una estrategia para reducir el trabajo de GPU, el siguiente paso es comprender las optimizaciones del motor en tiempo de ejecución y del controlador que se entornecen al generar perfiles.

El trabajo de CPU se puede dividir en tres depósitos: el trabajo de la aplicación, el trabajo en tiempo de ejecución y el trabajo del controlador. Ignore el trabajo de la aplicación, ya que está bajo control del programador. Desde el punto de vista de la aplicación, el tiempo de ejecución y el controlador son como las caja negra, ya que la aplicación no tiene control sobre lo que se implementa en ellas. La clave es comprender las técnicas de optimización que se pueden implementar en el tiempo de ejecución y el controlador. Si no entiende estas optimizaciones, es muy fácil saltar a una conclusión incorrecta sobre la cantidad de trabajo que la CPU está realizando en función de las medidas del perfil. En concreto, hay dos temas relacionados con algo denominado búfer de comandos y lo que puede hacer para ofuscar la generación de perfiles. Estos temas son:

-   Optimización en tiempo de ejecución con el búfer de comandos. El búfer de comandos es una optimización en tiempo de ejecución que reduce el impacto de una transición de modo. Para controlar el tiempo de la transición de modo, vea [Controlar el búfer de comandos](#controlling-the-command-buffer).
-   Negación de los efectos de control de tiempo del búfer de comandos. El tiempo transcurrido de una transición de modo puede tener un gran impacto en las medidas de generación de perfiles. La estrategia para esto es hacer que la secuencia de representación [sea grande en comparación con la transición de modo](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Controlar el búfer de comandos

Cuando una aplicación realiza una llamada API, el tiempo de ejecución convierte la llamada API a un formato independiente del dispositivo (al que llamaremos un comando) y la almacena en el búfer de comandos. El búfer de comandos se agrega al diagrama siguiente.

![diagrama de componentes de cpu, incluido un búfer de comandos](images/microbenchmarkcommandbuffer2.png)

Cada vez que la aplicación realiza otra llamada API, el tiempo de ejecución repite esta secuencia y agrega otro comando al búfer de comandos. En algún momento, el tiempo de ejecución vacía el búfer (enviando los comandos al controlador). En Windows XP, al vaciar el búfer de comandos se produce una transición de modo a medida que el sistema operativo cambia del entorno de ejecución (que se ejecuta en modo de usuario) al controlador (que se ejecuta en modo kernel), como se muestra en el diagrama siguiente.

-   modo de usuario: modo de procesador sin privilegios que ejecuta el código de la aplicación. Las aplicaciones en modo de usuario no pueden obtener acceso a los datos del sistema excepto a través de los servicios del sistema.
-   modo kernel: el modo de procesador con privilegios en el que Windows código ejecutivo basado en el kernel. Un controlador o subproceso que se ejecuta en modo kernel tiene acceso a toda la memoria del sistema, acceso directo al hardware y las instrucciones de CPU para realizar E/S con el hardware.

![diagrama de transiciones entre el modo de usuario y el modo kernel](images/microbenchmarkcommandbuffer3.png)

La transición se produce cada vez que la CPU cambia del modo de usuario al modo kernel (y viceversa) y el número de ciclos que requiere es grande en comparación con una llamada API individual. Si el tiempo de ejecución envió cada llamada API al controlador cuando se invocó, cada llamada API incurriría en el costo de una transición de modo.

En su lugar, el búfer de comandos es una optimización en tiempo de ejecución diseñada para reducir el costo efectivo de la transición de modo. El búfer de comandos pone en cola muchos comandos de controlador como preparación para una transición de modo único. Cuando el tiempo de ejecución agrega un comando al búfer de comandos, el control se devuelve a la aplicación. Un profiler no tiene ninguna manera de saber que los comandos del controlador probablemente ni siquiera se hayan enviado todavía al controlador. Como resultado, los números devueltos por un profiler de instrumentación fuera de uso son engañosos, ya que mide el trabajo en tiempo de ejecución, pero no el trabajo del controlador asociado.

### <a name="profile-results-without-a-mode-transition"></a>Resultados del perfil sin una transición de modo

Con la secuencia de representación del ejemplo 2, estas son algunas medidas de control de tiempo típicas que ilustran la magnitud de una transición de modo. Suponiendo que [**las llamadas SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) no provocan una transición de modo, un profiler de instrumentación estándar podría devolver resultados similares a los siguientes:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Cada uno de estos números es la cantidad de tiempo que tarda el runtime en agregar estas llamadas al búfer de comandos. Puesto que no hay ninguna transición de modo, el controlador aún no ha realizado ningún trabajo. Los resultados del profiler son precisos, pero no miden todo el trabajo que la secuencia de representación finalmente hará que la CPU realice.

### <a name="profile-results-with-a-mode-transition"></a>Resultados del perfil con una transición de modo

Ahora, mire lo que sucede en el mismo ejemplo cuando se produce una transición de modo. Esta vez, suponga [**que SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**y DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) provocan una transición de modo. Una vez más, un profiler de instrumentación fuera de la plataforma podría devolver resultados similares a los siguientes:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



El tiempo medido para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) es aproximadamente el mismo, pero el aumento drástico de la cantidad de tiempo empleado en [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) se debe a la transición del modo. Esto es lo que sucede:

1.  Suponga que el búfer de comandos tiene espacio para un comando antes de que se inicie la secuencia de representación.
2.  [**SetTexture se**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) convierte a un formato independiente del dispositivo y se agrega al búfer de comandos. En este escenario, esta llamada rellena el búfer de comandos.
3.  El tiempo de ejecución intenta agregar [**DrawPrimitive al**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) búfer de comandos, pero no puede, porque está lleno. En su lugar, el tiempo de ejecución vacía el búfer de comandos. Esto provoca la transición en modo kernel. Suponga que la transición tarda aproximadamente 5000 ciclos. Este tiempo contribuye al tiempo empleado en **DrawPrimitive.**
4.  A continuación, el controlador procesa el trabajo asociado a todos los comandos que se vaciaron del búfer de comandos. Suponga que el tiempo del controlador para procesar los comandos que casi llenan el búfer de comandos es de aproximadamente 935 000 ciclos. Suponga que el trabajo del controlador asociado a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) es de aproximadamente 2750 ciclos. Este tiempo contribuye al tiempo empleado en [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
5.  Cuando el controlador finaliza su trabajo, la transición de modo de usuario devuelve el control al tiempo de ejecución. El búfer de comandos ahora está vacío. Suponga que la transición tarda aproximadamente 5000 ciclos.
6.  La secuencia de representación finaliza al convertir [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) y agregarla al búfer de comandos. Supongamos que esto tarda aproximadamente 900 ciclos. Este tiempo contribuye al tiempo empleado en **DrawPrimitive.**

Para resumir los resultados, verá lo siguiente:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Al igual que la medida de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sin la transición de modo (900 ciclos), la medida para **DrawPrimitive** con la transición de modo (947 950 ciclos) es precisa, pero no sirve para presupuestos de trabajo de CPU. El resultado contiene el trabajo en tiempo de ejecución correcto, el trabajo del controlador para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), el trabajo del controlador para los comandos que precedieron a **SetTexture** y dos transiciones de modo. Sin embargo, a la medida le falta el trabajo del controlador **DrawPrimitive.**

Podría producirse una transición de modo en respuesta a cualquier llamada. Depende de lo que se encontraba anteriormente en el búfer de comandos. Debe controlar la transición de modo para comprender cuánto trabajo de CPU (tiempo de ejecución y controlador) está asociado a cada llamada. Para ello, necesita un mecanismo para controlar el búfer de comandos y el tiempo de la transición de modo.

### <a name="the-query-mechanism"></a>El mecanismo de consulta

El mecanismo de consulta de Microsoft Direct3D 9 se diseñó para permitir que el tiempo de ejecución consultara la GPU para ver el progreso y devolver determinados datos de la GPU. Durante la generación de perfiles, si el trabajo de GPU se minimiza para que tenga un impacto insignificante en el rendimiento, puede devolver el estado de la GPU para ayudar a medir el trabajo del controlador. Después de todo, el trabajo del controlador se completa cuando la GPU ha visto los comandos del controlador. Además, se puede hacer que el mecanismo de consulta controle dos características de búfer de comandos que son importantes para la generación de perfiles: cuando el búfer de comandos se vacía y cuánto trabajo hay en el búfer.

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



Ejemplo 3: Usar una consulta para controlar el búfer de comandos

Esta es una explicación más detallada de cada una de estas líneas de código:

1.  Cree una consulta de eventos mediante la creación de un objeto de consulta con D3DQUERYTYPE \_ EVENT.
2.  Agregue un marcador de evento de consulta al búfer de comandos mediante una llamada [**a Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ END**](d3dissue-end.md)). Este marcador indica al controlador que realice el seguimiento cuando la GPU termine de ejecutar los comandos anteriores al marcador.
3.  La primera llamada vacía el búfer de comandos porque llamar a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) obliga a vaciar el búfer de comandos. Cada llamada posterior está comprobando la GPU para ver cuándo finaliza el procesamiento de todo el trabajo del búfer de comandos. Este bucle no devuelve S \_ OK hasta que la GPU está inactiva.
4.  Muestrear la hora de inicio.
5.  Invoque las llamadas API de las que se está perfilado.
6.  Agregue un segundo marcador de evento de consulta al búfer de comandos. Este marcador se usará para realizar un seguimiento de la finalización de las llamadas.
7.  La primera llamada vacía el búfer de comandos porque llamar a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) obliga a vaciar el búfer de comandos. Cuando la GPU termina de procesar todo el trabajo del búfer de comandos, **GetData** devuelve S OK y el bucle se cierra porque la \_ GPU está inactiva.
8.  Muestrear la hora de detenerse.

Estos son los resultados medidos con QueryPerformanceCounter y QueryPerformanceFrequency:



| Variable local | Número de pasos |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| Freq           | 3579545         |



 

Convertir tics en ciclos una vez más (en una máquina de 2 GHz):


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



El mecanismo de consulta nos ha permitido controlar el tiempo de ejecución y el trabajo del controlador que se está mide. Para comprender cada uno de estos números, esto es lo que sucede en respuesta a cada una de las llamadas API, junto con los tiempos estimados:

1.  La primera llamada vacía el búfer de comandos mediante una llamada [**a GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md). Cuando la GPU termina de procesar todo el trabajo del búfer de comandos, **GetData** devuelve S OK y el bucle se cierra porque la \_ GPU está inactiva.
2.  La secuencia de representación comienza convirtiendo [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) a un formato independiente del dispositivo y agregándole al búfer de comandos. Suponga que esto tarda unos 100 ciclos.
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) se convierte y se agrega al búfer de comandos. Supongamos que esto tarda aproximadamente 900 ciclos.
4.  [**El problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) agrega un marcador de consulta al búfer de comandos. Suponga que esto tarda aproximadamente 200 ciclos.
5.  [**GetData hace**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) que el búfer de comandos se vacie, lo que fuerza la transición en modo kernel. Suponga que esto tarda aproximadamente 5000 ciclos.
6.  A continuación, el controlador procesa el trabajo asociado a las cuatro llamadas. Suponga que el tiempo del controlador para procesar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) es de aproximadamente 2964 ciclos, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) es de aproximadamente 3600 ciclos, [**el**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) problema es de unos 200 ciclos. Por lo tanto, el tiempo total del controlador para los cuatro comandos es de aproximadamente 6450 ciclos.
    > [!Note]  
    > El controlador también tarda un poco en ver cuál es el estado de la GPU. Dado que el trabajo de GPU es trivial, la GPU ya debe realizarse. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devolverá S \_ OK en función de la probabilidad de que la GPU haya finalizado.

     

7.  Cuando el controlador finaliza su trabajo, la transición de modo de usuario devuelve el control al tiempo de ejecución. El búfer de comandos ahora está vacío. Suponga que esto tarda aproximadamente 5000 ciclos.

Los números de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) incluyen:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



El mecanismo de consulta utilizado en combinación con QueryPerformanceCounter mide todo el trabajo de CPU. Esto se hace con una combinación de marcadores de consulta y comparaciones de estado de consulta. Los marcadores de consulta de inicio y detenerse agregados al búfer de comandos se usan para controlar la cantidad de trabajo que hay en el búfer. Al esperar hasta que se devuelve el código de retorno correcto, la medida de inicio se realiza justo antes de que se inicie una secuencia de representación limpia y la medida de detenerse se realiza justo después de que el controlador haya finalizado el trabajo asociado al contenido del búfer de comandos. Esto captura de forma eficaz el trabajo de CPU realizado por el tiempo de ejecución, así como el controlador.

Ahora que conoce el búfer de comandos y el efecto que puede tener en la generación de perfiles, debe saber que hay algunas otras condiciones que pueden hacer que el tiempo de ejecución vacíe el búfer de comandos. Debe estar atento a ellos en las secuencias de representación. Algunas de estas condiciones son en respuesta a las llamadas API y otras son respuesta a los cambios de recursos en el tiempo de ejecución. Cualquiera de las condiciones siguientes provocará una transición de modo:

-   Cuando se llama a uno de los métodos de bloqueo [**(Bloqueo)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)en un búfer de vértices, búfer de índice o textura (en determinadas condiciones con determinadas marcas).
-   Cuando se crea un búfer de dispositivo o vértice, búfer de índice o textura.
-   Cuando la última versión destruye un dispositivo o búfer de vértices, búfer de índice o textura.
-   Cuando [**se llama a ValidateDevice.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice)
-   Cuando se llama a [**Present.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   Cuando se llena el búfer de comandos.
-   Cuando [**se llama a GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con D3DGETDATA \_ FLUSH.

Tenga cuidado de observar estas condiciones en las secuencias de representación. Cada vez que se agrega una transición de modo, se agregarán 10 000 ciclos de trabajo del controlador a las medidas de generación de perfiles. Además, el búfer de comandos no tiene un tamaño estático. El tiempo de ejecución puede cambiar el tamaño del búfer en respuesta a la cantidad de trabajo que está generando la aplicación. Se trata de otra optimización que depende de una secuencia de representación.

Por lo tanto, tenga cuidado de controlar las transiciones de modo durante la generación de perfiles. El mecanismo de consulta ofrece un método sólido para vaciar el búfer de comandos para que pueda controlar el tiempo de la transición en modo, así como la cantidad de trabajo que contiene el búfer. Sin embargo, incluso esta técnica se puede mejorar reduciendo el tiempo de transición del modo para que sea insignificante con respecto al resultado medido.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Hacer que la secuencia de representación sea grande en comparación con la transición de modo

En el ejemplo anterior, el conmutador de modo kernel y el conmutador de modo de usuario consumen aproximadamente 10 000 ciclos que no tienen nada que ver con el tiempo de ejecución y el trabajo del controlador. Puesto que la transición de modo está integrada en el sistema operativo, no se puede reducir a cero. Para que la transición del modo sea insignificante, la secuencia de representación debe ajustarse para que el trabajo del controlador y el tiempo de ejecución sean un orden de magnitud mayor que los modificadores de modo. Puede intentar realizar una resta para quitar las transiciones, pero amortizar el costo con un costo de secuencia de representación mucho mayor es más confiable.

La estrategia para reducir la transición en modo hasta que sea insignificante es agregar un bucle a la secuencia de representación. Por ejemplo, echemos un vistazo a los resultados de generación de perfiles si se agrega un bucle que repetirá la secuencia de representación 1500 veces:


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



Ejemplo 4: Agregar un bucle a la secuencia de representación

Estos son los resultados medidos con QueryPerformanceCounter y QueryPerformanceFrequency:



| Variable local | Número de tics |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| Freq           | 3579545        |



 

El uso de QueryPerformanceCounter mide ahora 2840 tics. La conversión de tics en ciclos es la misma que ya se ha mostrado:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



En otras palabras, se necesitan unos 6,9 millones de ciclos en esta máquina de 2 GHz para procesar las 1500 llamadas en el bucle de representación. De los 6,9 millones de ciclos, la cantidad de tiempo en las transiciones en modo es aproximadamente de 10 000, por lo que ahora los resultados del perfil miden casi por completo el trabajo asociado a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**y DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)

Observe que el ejemplo de código requiere una matriz de dos texturas. Para evitar una optimización en tiempo de ejecución que quitaría [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) si establece el mismo puntero de textura cada vez que se llama, basta con usar una matriz de dos texturas. De este modo, cada vez que se pasa por el bucle, cambia el puntero de textura y se realiza el trabajo completo asociado a **SetTexture.** Asegúrese de que ambas texturas tienen el mismo tamaño y formato, de modo que ningún otro estado cambie cuando lo haga la textura.

Y ahora tiene una técnica para generar perfiles de Direct3D. Se basa en el contador de alto rendimiento (QueryPerformanceCounter) para registrar el número de pasos que tarda la CPU en procesar el trabajo. El trabajo se controla cuidadosamente para que sea el tiempo de ejecución y el trabajo del controlador asociados a las llamadas API mediante el mecanismo de consulta. Una consulta proporciona dos medios de control: primero para vaciar el búfer de comandos antes de que se inicie la secuencia de representación y, en segundo lugar, para devolver cuando finalice el trabajo de GPU.

Hasta ahora, en este documento se ha mostrado cómo crear perfiles de una secuencia de representación. Cada secuencia de representación ha sido bastante sencilla, con una sola [**llamada DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) y una [**llamada SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Esto se hizo para centrarse en el búfer de comandos y en el uso del mecanismo de consulta para controlarlo. Este es un breve resumen de cómo crear perfiles de una secuencia de representación arbitraria:

-   Use un contador de alto rendimiento como QueryPerformanceCounter para medir el tiempo necesario para procesar cada llamada API. Use QueryPerformanceFrequency y la velocidad del reloj de CPU para convertirla en el número de ciclos de CPU por llamada API.
-   Minimice la cantidad de trabajo de GPU mediante la representación de listas de triángulos, donde cada triángulo contiene un píxel.
-   Use el mecanismo de consulta para vaciar el búfer de comandos antes de la secuencia de representación. Esto garantiza que la generación de perfiles capturará la cantidad correcta de tiempo de ejecución y el trabajo del controlador asociados a la secuencia de representación.
-   Controlar la cantidad de trabajo agregado al búfer de comandos con marcadores de eventos de consulta. Esta misma consulta detecta cuándo finaliza su trabajo la GPU. Dado que el trabajo de GPU es trivial, esto es prácticamente equivalente a medir cuándo se completa el trabajo del controlador.

Todas estas técnicas se usan para crear perfiles de los cambios de estado. Suponiendo que ha leído y comprendido cómo controlar el búfer de comandos y que ha completado correctamente las medidas de línea base en [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)está listo para agregar cambios de estado a las secuencias de representación. Hay algunos desafíos adicionales de generación de perfiles al agregar cambios de estado a una secuencia de representación. Si piensa agregar cambios de estado a las secuencias de representación, asegúrese de continuar en la sección siguiente.

## <a name="profiling-direct3d-state-changes"></a>Generar perfiles de cambios de estado de Direct3D

Direct3D usa muchos estados de representación para controlar casi todos los aspectos de la canalización. Las API que provocan cambios de estado incluyen cualquier función o método que no sea las llamadas \* primitivas de Draw.

Los cambios de estado son complicados porque es posible que no pueda ver el costo de un cambio de estado sin representación. Esto es el resultado del algoritmo diferido que el controlador y la GPU usan para aplazar el trabajo hasta que sea absolutamente necesario. En general, debe seguir estos pasos para medir un único cambio de estado:

1.  Cuadro [**de perfilPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) en primer lugar.
2.  Agregue un cambio de estado a la secuencia de representación y desenlaza la nueva secuencia.
3.  Resta la diferencia entre las dos secuencias para obtener el costo del cambio de estado.

Por supuesto, todo lo que ha aprendido sobre el uso del mecanismo de consulta y la colocación de la secuencia de representación en un bucle para negar el costo de la transición en modo todavía se aplica.

### <a name="profiling-a-simple-state-change"></a>Generación de perfiles de un cambio de estado simple

A partir de una secuencia de representación que contiene [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)esta es la secuencia de código para medir el costo de agregar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):


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



Ejemplo 5: Medición de una llamada API de cambio de estado

Observe que el bucle contiene dos llamadas, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) La secuencia de representación recorre en bucle 1500 veces y genera resultados similares a estos:



| Variable local | Número de tics |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| Freq           | 3579545        |



 

La conversión de tics en ciclos una vez más produce:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



La división por el número de iteraciones del bucle produce:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Cada iteración del bucle contiene un cambio de estado y una llamada a draw. Restando el resultado de las hojas de la secuencia de representación [**DrawPrimitive:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
3850 - 1100 = 2750 cycles for SetTexture
```



Este es el número medio de ciclos para agregar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) a esta secuencia de representación. Esta misma técnica se puede aplicar a otros cambios de estado.

¿Por [**qué setTexture se**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) denomina un cambio de estado simple? Dado que el estado que se establece está restringido para que la canalización haga la misma cantidad de trabajo cada vez que se cambia el estado. Restringir ambas texturas al mismo tamaño y formato garantiza la misma cantidad de trabajo para cada **llamada a SetTexture.**

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Generación de perfiles de un cambio de estado que debe alternarse

Hay otros cambios de estado que hacen que la cantidad de trabajo realizado por la canalización de gráficos cambie para cada iteración del bucle de representación. Por ejemplo, si la prueba z está habilitada, cada color de píxel actualiza un destino de representación solo después de que se prueba el valor z del nuevo píxel con respecto al valor z del píxel existente. Si la prueba z está deshabilitada, esta prueba por píxel no se realiza y la salida se escribe mucho más rápido. La habilitación o deshabilitación del estado de prueba z cambia drásticamente la cantidad de trabajo realizado (tanto por la CPU como por la GPU) durante la representación.

[**SetRenderState requiere**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) un estado de representación determinado y un valor de estado para habilitar o deshabilitar las pruebas z. El valor de estado concreto se evalúa en tiempo de ejecución para determinar cuánto trabajo es necesario. Es difícil medir este cambio de estado en un bucle de representación y seguir condición previamente el estado de la canalización para que cambie. La única solución es alternar el cambio de estado durante la secuencia de representación.

Por ejemplo, la técnica de generación de perfiles debe repetirse dos veces como se muestra a continuación:

1.  Empiece generando perfiles de la secuencia de [**representación DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Llámelo línea base.
2.  Generación de perfiles de una segunda secuencia de representación que alterna el cambio de estado. El bucle de secuencia de representación contiene:
    -   Un cambio de estado para establecer el estado en una condición "false".
    -   [**DrawPrimitive igual**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) que la secuencia original.
    -   Un cambio de estado para establecer el estado en una condición "true".
    -   Un segundo [**DrawPrimitive para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) forzar la realización del segundo cambio de estado.
3.  Busque la diferencia entre las dos secuencias de representación. Para hacer esto:
    -   Multiplique la [**secuencia DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de línea base por 2 porque hay dos llamadas **DrawPrimitive** en la nueva secuencia.
    -   Resta el resultado de la nueva secuencia de la secuencia original.
    -   Divida el resultado entre 2 para obtener el costo medio del cambio de estado "false" y "true".

Con la técnica de bucle usada en la secuencia de representación, el costo de cambiar el estado de la canalización debe medirse cambiando el estado de una condición "true" a una condición "false" y viceversa, para cada iteración de la secuencia de representación. El significado de "true" y "false" aquí no es literal, simplemente significa que el estado debe establecerse en condiciones opuestas. Esto hace que ambos cambios de estado se miden durante la generación de perfiles. Por supuesto, todo lo que ha aprendido sobre el uso del mecanismo de consulta y la colocación de la secuencia de representación en un bucle para negar el costo de la transición en modo todavía se aplica.

Por ejemplo, esta es la secuencia de código para medir el costo de alternar las pruebas z on o off:


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



Ejemplo 5: Medición de un cambio de estado de alternar

El bucle alterna el estado mediante la ejecución de dos [**llamadas SetRenderState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) La primera **llamada a SetRenderState** deshabilita las pruebas z y la segunda **setRenderState** habilita las pruebas z. Cada **SetRenderState** va seguido de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para que el controlador procese el trabajo asociado al cambio de estado en lugar de establecer solo un bit desaprobado en el controlador.

Estos números son razonables para esta secuencia de representación:



| Variable local | Número de pasos |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| Freq           | 3579545         |



 

La conversión de tics en ciclos una vez más produce:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



La división por el número de iteraciones del bucle produce:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Cada iteración del bucle contiene dos cambios de estado y dos llamadas a draw. Restar las llamadas a draw (suponiendo que hay 1100 ciclos) deja:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Este es el número medio de ciclos para ambos cambios de estado, por lo que el tiempo medio para cada cambio de estado es:


```
4000 / 2  = 2000 cycles for each state change
```



Por lo tanto, el número medio de ciclos para habilitar o deshabilitar las pruebas z es de 2000 ciclos. Merece la pena tener en cuenta que QueryPerformanceCounter mide z-enable la mitad del tiempo y z-disable la mitad del tiempo. Esta técnica mide realmente el promedio de ambos cambios de estado. En otras palabras, está midiendo el tiempo para alternar un estado. Con esta técnica, no tiene ninguna manera de saber si los tiempos de habilitación y deshabilitación son equivalentes, ya que ha medido el promedio de ambos. No obstante, se trata de un número razonable que se puede usar al presupuestar un estado de modificación como una aplicación que provoca este cambio de estado solo puede hacerlo cambiando este estado.

Ahora puede aplicar estas técnicas y crear perfiles de todos los cambios de estado que desee, ¿no? No del todo. Todavía debe tener cuidado con las optimizaciones diseñadas para reducir la cantidad de trabajo que debe realizarse. Hay dos tipos de optimizaciones que debe tener en cuenta al diseñar las secuencias de representación.

### <a name="watch-out-for-state-change-optimizations"></a>Esté atento a las optimizaciones de cambios de estado

En la sección anterior se muestra cómo generar perfiles de ambos tipos de cambios de estado: un cambio de estado simple que está restringido para generar la misma cantidad de trabajo para cada iteración y un cambio de estado de alternar que cambia drásticamente la cantidad de trabajo realizado. ¿Qué ocurre si toma la secuencia de representación anterior y le agrega otro cambio de estado? Por ejemplo, en este ejemplo se toma la secuencia de representación> habilitar z y se le agrega una comparación z-func:


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



El estado z-func establece el nivel de comparación al escribir en el búfer z (entre el valor z de un píxel actual con el valor z de un píxel en el búfer de profundidad). D3DCMP NUNCA desactiva la comparación de pruebas z, mientras que D3DCMP SIEMPRE establece que la comparación se haga cada vez que se realiza \_ \_ la prueba z.

La generación de perfiles de cualquiera de estos cambios de estado en una secuencia de representación [**con DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) genera resultados similares a estos:



| Cambio de estado único | Promedio de ciclos |
|---------------------|--------------------------|
| Solo D3DRS \_ ZENABLE | 2000                     |



 

or



| Cambio de estado único | Promedio de ciclos |
|---------------------|--------------------------|
| Solo D3DRSUNC \_   | 600                      |



 

Sin embargo, si genera perfiles de D3DRS ZENABLE y \_ D3DRS RAGUNC en la misma secuencia de representación, podría ver resultados \_ como estos:



| Ambos cambios de estado            | Promedio de ciclos |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRSUNC \_ | 2000                     |



 

Puede esperar que el resultado sea la suma de 2000 y 600 ciclos (o 2600) porque el controlador está realizando todo el trabajo asociado con la configuración de ambos estados de representación. En su lugar, el promedio es de 2000 ciclos.

Este resultado refleja una optimización de cambio de estado implementada en el tiempo de ejecución, el controlador o la GPU. En este caso, el controlador podría ver el primer [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y establecer un estado de desarroba que pospondría el trabajo hasta más adelante. Cuando el controlador ve el segundo **SetRenderState,** se podría establecer de forma redundante el mismo estado de des dirty y el mismo trabajo se pospondría una vez más. Cuando [**se llama a DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) finalmente se procesa el trabajo asociado al estado de des dirty. El controlador ejecuta el trabajo una vez, lo que significa que el controlador consolida eficazmente los dos primeros cambios de estado. Del mismo modo, el controlador consolida eficazmente los cambios de estado tercero y cuarto en un único cambio de estado cuando se llama al segundo **DrawPrimitive.** El resultado neto es que el controlador y la GPU procesan un único cambio de estado para cada llamada a draw.

Este es un buen ejemplo de optimización de controladores dependientes de la secuencia. El controlador pospone el trabajo dos veces estableciendo un estado de desarroba y, a continuación, realiza el trabajo una vez para borrar el estado de des dirty. Este es un buen ejemplo del tipo de mejora de la eficacia que puede tener lugar cuando el trabajo se aplaza hasta que sea absolutamente necesario.

¿Cómo sabe qué cambios de estado establecen un estado desaplazado internamente y, por tanto, posponen el trabajo hasta más adelante? Solo probando secuencias de representación (o hablando con escritores de controladores). Los controladores se actualizan y mejoran periódicamente, por lo que la lista de optimizaciones no es estática. Solo hay una manera de saber absolutamente lo que cuesta un cambio de estado en una secuencia de representación determinada, en un conjunto determinado de hardware. y que es para medirlo.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Cuidado con las optimizaciones DrawPrimitive

Además de las optimizaciones de cambios de estado, el tiempo de ejecución intentará optimizar el número de llamadas a draw que el controlador tiene que procesar. Por ejemplo, considere estas llamadas a back-draw:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Ejemplo 5a: dos llamadas a Draw

Esta secuencia contiene dos llamadas a draw, que el tiempo de ejecución consolidará en una sola llamada equivalente a:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Ejemplo 5b: una sola llamada a draw concatenada

El tiempo de ejecución concatenará ambas llamadas a draw concretas en una sola llamada, lo que reduce el trabajo del controlador en un 50 %, ya que el controlador solo tendrá que procesar una llamada a draw.

En general, el tiempo de ejecución concatenará dos o más llamadas [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de back-to-back cuando:

1.  El tipo primitivo es una lista de triángulos (D3DPT \_ TRIANGLELIST).
2.  Cada llamada [**a DrawPrimitive sucesiva**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) debe hacer referencia a vértices consecutivos dentro del búfer de vértices.

De forma similar, las condiciones adecuadas para concatenar dos o más llamadas [**drawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) de back-to-back son:

1.  El tipo primitivo es una lista de triángulos (D3DPT \_ TRIANGLELIST).
2.  Cada llamada [**a DrawIndexedPrimitive sucesiva**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) debe hacer referencia secuencialmente a índices consecutivos dentro del búfer de índice.
3.  Cada llamada [**a DrawIndexedPrimitive sucesiva**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) debe usar el mismo valor para BaseVertexIndex.

Para evitar la concatenación durante la generación de perfiles, modifique la secuencia de representación para que el tipo primitivo no sea una lista de triángulos, o modifique la secuencia de representación para que no haya llamadas de dibujo hacia atrás que usen vértices consecutivos (o índices). Más concretamente, el tiempo de ejecución también concatenará las llamadas a draw que cumplen las dos condiciones siguientes:

-   Cuando la llamada anterior es [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), si la siguiente llamada a draw:
    -   usa una lista de triángulos, AND
    -   especifica startVertex = anterior StartVertex + PrimitiveCount \* 3 anterior
-   Al usar [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), si la siguiente llamada a draw:
    -   usa una lista de triángulos, AND
    -   especifica startIndex = previous StartIndex + previous PrimitiveCount \* 3, AND
    -   especifica baseVertexIndex = basevertexindex anterior

Este es un ejemplo más sutil de concatenación de llamadas a draw que es fácil de pasar por alto al generar perfiles. Supongamos que la secuencia de representación tiene el siguiente aspecto:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Ejemplo 5c: Un cambio de estado y una llamada a Draw

El bucle recorre en iteración 1500 triángulos, estableciendo una textura y dibujando cada triángulo. Este bucle de representación tarda aproximadamente 2750 ciclos para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) y 1100 ciclos para [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) como se muestra en las secciones anteriores. Puede esperar intuitivamente que mover **SetTexture** fuera del bucle de representación reduzca la cantidad de trabajo realizado por el controlador en 1500 2750 ciclos, que es la cantidad de trabajo asociada a llamar a \* **SetTexture** 1500 veces. El fragmento de código tendría el siguiente aspecto:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Ejemplo 5d: Ejemplo 5c con el cambio de estado fuera del bucle

Mover [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) fuera del bucle de representación reduce la cantidad de trabajo asociado a **SetTexture,** ya que se llama una vez en lugar de 1500 veces. Un efecto secundario menos obvio es que el trabajo de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) también se reduce de 1500 llamadas a 1 llamada porque se cumplen todas las condiciones para concatenar llamadas a draw. Cuando se procesa la secuencia de representación, el tiempo de ejecución procesará 1500 llamadas en una sola llamada de controlador. Al mover esta línea de código, la cantidad de trabajo del controlador se ha reducido drásticamente:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Estos resultados son completamente correctos, pero son muy confusos en el contexto de la pregunta original. La optimización de llamadas a draw ha provocado que la cantidad de trabajo del controlador se reduzca drásticamente. Se trata de un problema común al realizar la generación de perfiles personalizada. Al eliminar las llamadas de una secuencia de representación, tenga cuidado de evitar la concatenación de llamadas a draw. De hecho, este escenario es un ejemplo eficaz de la cantidad de mejora en el rendimiento del controlador posible por esta optimización en tiempo de ejecución.

Por lo tanto, ahora sabe cómo medir los cambios de estado. Empiece generando [**perfiles drawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) A continuación, agregue cada cambio de estado adicional a la secuencia (en algunos casos agregando una llamada y, en otros casos, agregando dos llamadas) y mida la diferencia entre las dos secuencias. Puede convertir los resultados en tics, ciclos o tiempo. Al igual que la medición de secuencias de representación con QueryPerformanceCounter, la medición de los cambios de estado individuales se basa en el mecanismo de consulta para controlar el búfer de comandos y colocar los cambios de estado en un bucle para minimizar el impacto de las transiciones en modo. Esta técnica mide el costo de alternar un estado, ya que el profiler devuelve el promedio de habilitación y deshabilitación del estado.

Con esta funcionalidad, puede empezar a generar secuencias de representación arbitrarias y medir con precisión el tiempo de ejecución asociado y el trabajo del controlador. A continuación, los números se pueden usar para responder a preguntas presupuestadas, como "cuántas más de estas llamadas" se pueden realizar en la secuencia de representación mientras se mantiene una velocidad de fotogramas razonable, suponiendo escenarios con CPU limitada.

## <a name="summary"></a>Resumen

En este documento se muestra cómo controlar el búfer de comandos para que se puedan perfiles de llamadas individuales con precisión. Los números de generación de perfiles se pueden generar en tics, ciclos o tiempo absoluto. Representan la cantidad de tiempo de ejecución y el trabajo del controlador asociados a cada llamada API.

Empiece generando perfiles de una llamada \* a Draw Primitive en una secuencia de representación. Recuerde:

1.  Use QueryPerformanceCounter para medir el número de tics por llamada API. Use QueryPerformanceFrequency para convertir los resultados en ciclos u horas si lo desea.
2.  Use el mecanismo de consulta para vaciar el búfer de comandos antes de iniciar.
3.  Incluya la secuencia de representación en un bucle para minimizar el impacto de la transición en modo.
4.  Use el mecanismo de consulta para medir cuándo la GPU ha completado su trabajo.
5.  Tenga cuidado con la concatenación en tiempo de ejecución que tendrá un impacto importante en la cantidad de trabajo realizado.

Esto proporciona un rendimiento de línea de base [**para DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) que se puede usar para compilar. Para perfiles de un cambio de estado, siga estas sugerencias adicionales:

1.  Agregue el cambio de estado a un perfil de secuencia de representación conocido de la nueva secuencia. Puesto que las pruebas se realizan en un bucle, esto requiere establecer el estado dos veces en valores opuestos (como habilitar y deshabilitar por ejemplo).
2.  Compare la diferencia en los tiempos de ciclo entre las dos secuencias.
3.  Para los cambios de estado que cambian significativamente la canalización (como [**SetTexture),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)resta la diferencia entre las dos secuencias para obtener el tiempo para el cambio de estado.
4.  Para los cambios de estado que cambian significativamente la canalización (y, por lo tanto, requieren alternar estados como [**SetRenderState),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)resta la diferencia entre las secuencias de representación y divida entre 2. Esto generará el número medio de ciclos para cada cambio de estado.

Pero tenga cuidado con las optimizaciones que provocan resultados inesperados al generar perfiles. Las optimizaciones de cambios de estado pueden establecer estados desaplazados, lo que hace que el trabajo se aplaza. Esto puede provocar resultados del perfil que no son tan intuitivos como se esperaba. Las llamadas a draw que se concatenan reducirán drásticamente el trabajo del controlador, lo que puede dar lugar a conclusiones erróneas. Las secuencias de representación planeadas cuidadosamente se usan para evitar que se produzcan concatenaciones de llamadas de dibujo y cambio de estado. El truco es evitar que las optimizaciones se generen durante la generación de perfiles para que los números que genere sean números de presupuesto razonables.

> [!Note]  
> Duplicar esta estrategia de generación de perfiles en una aplicación sin el mecanismo de consulta es más difícil. Antes de Direct3D 9, la única manera predecible de vaciar el búfer de comandos es bloquear una superficie activa (como un destino de representación) para esperar hasta que la GPU esté inactiva. Esto se debe a que el bloqueo de una superficie obliga al tiempo de ejecución a vaciar el búfer de comandos en caso de que haya comandos de representación en el búfer que deba actualizar la superficie antes de que se bloquee, además de esperar a que finalice la GPU. Esta técnica es funcional, aunque es más obtrusiva que usar el mecanismo de consulta introducido en Direct3D 9.

 

## <a name="appendix"></a>Apéndice

Los números de esta tabla son una serie de aproximaciones para la cantidad de tiempo de ejecución y trabajo del controlador asociados a cada uno de estos cambios de estado. Las aproximaciones se basan en medidas reales realizadas en los controladores mediante las técnicas que se muestran en el documento. Estos números se generaron mediante el entorno de ejecución de Direct3D 9 y dependen del controlador.

Las técnicas de este documento están diseñadas para medir el tiempo de ejecución y el trabajo del controlador. En general, no es práctico proporcionar resultados que coincidan con el rendimiento de la CPU y la GPU en cada aplicación, ya que esto requeriría una matriz exhaustiva de secuencias de representación. Además, es especialmente difícil realizar pruebas comparativas del rendimiento de la GPU porque depende en gran medida del estado configurado en la canalización antes de la secuencia de representación. Por ejemplo, habilitar la mezcla alfa no afecta poco a la cantidad de trabajo de CPU necesario, pero puede tener un gran impacto en la cantidad de trabajo realizado por la GPU. Por lo tanto, las técnicas de este documento restringen el trabajo de GPU a la cantidad mínima posible limitando la cantidad de datos que se deben representar. Esto significa que los números de la tabla coincidirán más estrechamente con los resultados obtenidos de las aplicaciones que tienen cpu limitada (en lugar de una aplicación que está limitada por la GPU).

Se recomienda usar las técnicas presentadas para cubrir los escenarios y configuraciones más importantes para usted. Los valores de la tabla se pueden usar para compararlos con los números generados. Dado que cada controlador varía, la única manera de generar los números reales que verá es generar resultados de generación de perfiles mediante sus escenarios.



| Llamada a la API                             | Número medio de ciclos |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500 - 11250             |
| SetFVF                               | 6400 - 11200             |
| SetVertexShader                      | 3000 - 12100             |
| SetPixelShader                       | 6300 - 7000              |
| SPECULARENABLE                       | 1900 - 11200             |
| SetRenderTarget                      | 6000 - 6250              |
| SetPixelShaderConstant (1 constante)  | 1500 - 9000              |
| NORMALIZENORMALS                     | 2200 - 8100              |
| LightEnable                          | 1300 - 9000              |
| SetStreamSource                      | 3700 - 5800              |
| ILUMINACIÓN                             | 1700 - 7500              |
| DIFUSOMATERIALSOURCE                | 900 - 8300               |
| AMBIENTMATERIALSOURCE                | 900 - 8200               |
| COLORVERTEX                          | 800 - 7800               |
| SetLight                             | 2200 - 5100              |
| SetTransform                         | 3200 - 3750              |
| SetIndices                           | 900 - 5600               |
| AMBIENTE                              | 1150 - 4800              |
| SetTexture                           | 2500 - 3100              |
| SPECULARMATERIALSOURCE               | 900 - 4600               |
| EMISSIVEMATERIALSOURCE               | 900 - 4500               |
| SetMaterial                          | 1000 - 3700              |
| ZENABLE                              | 700 - 3900               |
| WRAP0                                | 1600 - 2700              |
| MINFILTER                            | 1700 - 2500              |
| MAGFILTER                            | 1700 - 2400              |
| SetVertexShaderConstant (1 constante) | 1000 - 2700              |
| COLOROP                              | 1500 - 2100              |
| COLORARG2                            | 1300 - 2000              |
| COLORARG1                            | 1300 - 1980              |
| CULLMODE                             | 500 - 2570               |
| RECORTE                             | 500 - 2550               |
| DrawIndexedPrimitive                 | 1200 - 1400              |
| ADDRESSV                             | 1090 - 1500              |
| ADDRESSU                             | 1070 - 1500              |
| DrawPrimitive                        | 1050 - 1150              |
| SRGBTEXTURE                          | 150 - 1500               |
| STENCILMASK                          | 570 - 700                |
| STENCILZFAIL                         | 500 - 800                |
| STENCILREF                           | 550 - 700                |
| ALPHABLENDENABLE                     | 550 - 700                |
| STENCILFUNC                          | 560 - 680                |
| STENCILWRITEMASK                     | 520 - 700                |
| STENCINCINCIIL                          | 500 - 750                |
| UNCUNC                                | 510 - 700                |
| ZWRITEENABLE                         | 520 - 680                |
| STENCILENABLE                        | 540 - 650                |
| STENCILPASS                          | 560 - 630                |
| SRCBLEND                             | 500 - 685                |
| \_StencilMODE de \_ dos lados              | 450 - 590                |
| ALPHATESTENABLE                      | 470 - 525                |
| ALPHAREF                             | 460 - 530                |
| ALPHAFUNC                            | 450 - 540                |
| DESTBLEND                            | 475 - 510                |
| COLORWRITEENABLE                     | 465 - 515                |
| CCW \_ STENCINCIIL                     | 340 - 560                |
| CCW \_ STENCILPASS                     | 340 - 545                |
| CCW \_ STENCILZFAIL                    | 330 - 495                |
| LAPRUEBATESTENABLE                    | 375 - 440                |
| CCW \_ STENCILFUNC                     | 250 - 480                |
| SetScissorRect                       | 150 - 340                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 
