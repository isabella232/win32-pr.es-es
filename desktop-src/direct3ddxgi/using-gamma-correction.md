---
description: Corrección gamma, o gamma para abreviar, es el nombre de una operación no lineal que los sistemas usan para codificar y descodificar los valores de píxeles de las imágenes.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Usar corrección gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c940db1a94fb41e9babecbeb3075aa9e01b3732
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552387"
---
# <a name="using-gamma-correction"></a>Usar corrección gamma

Corrección gamma, o gamma para abreviar, es el nombre de una operación no lineal que los sistemas usan para codificar y descodificar los valores de píxeles de las imágenes.

-   [¿Qué es gamma y para qué sirve?](#what-is-gamma-and-what-is-it-for)
-   [Fondo de gamma en Windows](#background-of-gamma-on-windows)
-   [Evolución del hardware de pantalla](#evolution-of-display-hardware)
-   [Funcionalidades de control gamma en DXGI](#gamma-control-capabilities-in-dxgi)
-   [Establecer el control gamma con DXGI](#setting-gamma-control-with-dxgi)
-   [Prácticas de control gamma](#gamma-control-practicalities)
-   [Temas relacionados](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>¿Qué es gamma y para qué sirve?

Al final de la canalización de gráficos, en el que la imagen deja el equipo para que realice su viaje a lo largo del cable del monitor, hay una pequeña parte del hardware que puede transformar los valores de píxel sobre la marcha. Este hardware suele usar una tabla de búsqueda para transformar los píxeles. Este hardware usa los valores rojo, verde y azul que provienen de la superficie que se va a mostrar para buscar valores corregidos en gamma en la tabla y, a continuación, envía los valores corregidos al monitor en lugar de los valores reales de la superficie. Por lo tanto, esta tabla de búsqueda es una oportunidad para reemplazar cualquier color por cualquier otro color. Aunque la tabla tiene ese nivel de potencia, el uso típico consiste en ajustar las imágenes sutilmente para compensar las diferencias en la respuesta del monitor. La respuesta del monitor es la función que relaciona el valor numérico de los componentes rojo, verde y azul de un píxel con el brillo mostrado de ese píxel.

Este es el objetivo de esta tabla, pero los desarrolladores de juegos encontraron usos creativos para ello, como la intermitencia de la pantalla entera para el efecto psicológico. En las aplicaciones de juegos modernas, como parte del procesamiento posterior de cada fotograma, normalmente proporcionamos otras maneras de realizar estas tareas. De hecho, se recomienda dejar la tabla gamma por sí sola, ya que podría estar en uso para calibrar la respuesta del monitor y los cambios más mayorista en la rampa de gamma destruirán esta rápida calibración.

La ciencia de la determinación de la corrección gamma es compleja y no se presenta aquí, excepto para iluminar la procedencia del nombre "gamma". Una respuesta de monitor CRT (es decir, una luna antigua) es una función compleja, pero la física de estos monitores significa que muestran una respuesta que se puede representar de forma bruta con esta función de potencia:

brillo (entrada) =<sup>Gamma</sup> de entrada

Normalmente, el valor gamma está cerca de un valor de 2,0. Los monitores LCD y todas las demás tecnologías más recientes se han diseñado específicamente para presentar una respuesta similar para que no sea necesario volver a calibrar el software y las imágenes para esas nuevas tecnologías. El estándar sRGB declara que este valor gamma es exactamente 2,2 y este valor se ha convertido en un estándar ampliamente implementado.

El ojo humano también tiene una función de respuesta que invierte aproximadamente la función de potencia de CRT. Esto significa que el brillo percibido de un píxel aumenta de forma lineal con los valores RGB de ese píxel.

Dado que un valor gamma de 2,2 se ha convertido en un estándar de facto, normalmente no es necesario preocuparse demasiado sobre la curva gamma codificada en esta tabla, y puede dejarla como una asignación lineal de uno a uno. La coincidencia de color adecuada requiere Exquisite Care con esta función, pero ese debate está fuera del ámbito de este tema. Windows incluye una herramienta que permite a los usuarios calibrar sus pantallas a gamma 2,2, y esta herramienta usa el hardware de la tabla de búsqueda para derivar un ajuste sutil elegido cuidadosamente para sus equipos. Los usuarios pueden ejecutar esta herramienta buscando "calibrar color". También hay perfiles de color bien definidos para monitores concretos que automatizan este proceso. La herramienta "calibrar color" puede detectar estos monitores más recientes e informar a los usuarios de que ya se ha implementado la calibración.

Esta noción de codificación de una ley de energía en valores de color es útil en otro lugar de la canalización de gráficos, especialmente en las texturas. En el caso de las texturas, querrá más precisión en los colores más oscuros debido a la respuesta del ojo humano logarítmico que acabo de hablar. Es importante un control cuidadoso de gamma en esta parte de la canalización. Para obtener más información, vea [convertir datos para el espacio de colores](converting-data-color-space.md).

El resto de este tema se centra solo en la corrección gamma en esta última parte de la canalización, entre los datos de búfer de fotogramas y el monitor. Si desea escribir un asistente para calibrado o crear efectos especiales en una aplicación de pantalla completa en la que un paso posterior al procesamiento no sea práctico, esta es la información que necesita.

## <a name="background-of-gamma-on-windows"></a>Fondo de gamma en Windows

Normalmente, los equipos de Windows tienen una tabla gamma que es una tabla de búsqueda que toma un triple de bytes y genera un triple de bytes. Estas triples son 768 (256 x 3) bytes de RAM. Esto es correcto cuando el formato de presentación contiene un triple de valores de BYTE RGB pero no es lo suficientemente expresivo como para describir las transformaciones que podría desear cuando el formato de presentación tiene un intervalo mayor que \[ 0, 1 \] , como los valores de punto flotante. Las API de Windows que controlan la gamma han seguido una evolución, ya que los formatos de visualización se han vuelto más complejos.

Las primeras API de Windows que ofrecen control gamma son [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) y [**GetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)de Windows interfaz de dispositivo gráfico (GDI). Estas API funcionan con matrices de palabras 3 256, donde cada palabra codifica en cero hasta una, representada por los valores 0 y 65535 de WORD. Normalmente, la precisión adicional de una palabra no está disponible en las tablas de búsqueda de hardware reales, pero estas API están diseñadas para ser flexibles. Estas API, a diferencia de las demás que se describen más adelante en esta sección, permiten solo una pequeña desviación de una función de identidad. De hecho, cualquier entrada en la rampa debe estar dentro de 32768 del valor de identidad. Esta restricción significa que ninguna aplicación puede activar la pantalla completamente en negro o en otro color ilegible.

La siguiente API es [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)de Microsoft Direct3D 9, que sigue el mismo patrón y formato de datos que [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp). El valor predeterminado de la rampa gamma de Direct3D 9 no es especialmente útil; es una rampa de palabras inicializadas en 0-255, no 0-65535, aunque la API esté definida en términos de 0-65535.

La API más reciente es [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol). Esta API tiene un esquema más flexible para expresar el control gamma, tal y como se ajusta al conjunto de formatos de presentación de DXGI, incluidos diez formatos enteros de bits por canal y de 16 bits y el \_ formato de intervalo extendido de polarización de XR.

Todas estas API operan en el mismo hardware y cambian los mismos valores. Las API de Direct3D 9 y DXGI son de solo escritura. No puede leer el valor del hardware, modificarlo y, a continuación, configurarlo. Solo puede establecer la rampa. Además, solo puede establecer gamma cuando la aplicación está en pantalla completa. Esta restricción es otra manera de garantizar que el escritorio sea siempre legible. Es decir, la aplicación puede afectar a su propia presentación, pero Windows restaurará la rampa gamma anterior cuando la aplicación pierda la pantalla completa (por ejemplo, mediante ALT-TAB o Ctrl-Alt-Supr).

## <a name="evolution-of-display-hardware"></a>Evolución del hardware de pantalla

Algunos monitores más recientes pueden mostrar una amplia gama de intensidades. Sin embargo, cuando el formato de presentación puede representar solo valores entre cero y uno, la pantalla debe asignar cero a su valor más oscuro y de uno a su valor más brillante. Este valor más brillante podría ser mucho más brillante para ver de forma cómoda las páginas web con texto en negro sobre un fondo blanco, pero es estupendo para efectos especiales demasiado brillantes, como ver la luz solar glittering de un lago o un relámpago bifurcar el cielo. Por lo tanto, necesitamos una manera de expresar estos intervalos más amplios. DXGI 1,1 y versiones posteriores contienen valores de formato de presentación que permiten que 1,0 represente un valor blanco confortable y Reserve valores de formato de presentación más amplios para efectos especiales demasiado brillantes. DXGI 1,1 admite dos formatos de presentación que pueden expresar estos valores más amplios: el formato de DXGI \_ \_ R10G10B10 \_ XR \_ \_ \_ UNORM y el punto flotante de 16 bits. Para obtener una descripción completa de estos formatos, consulte [los detalles del formato extendido](/windows-hardware/drivers/display/details-of-the-extended-format). A continuación, veremos por qué la API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) gamma de DXGI necesita valores de píxeles mayores que 1,0.

## <a name="gamma-control-capabilities-in-dxgi"></a>Funcionalidades de control gamma en DXGI

DXGI permite que el controlador de pantalla exprese sus controles gamma como una función lineal en pasos. Esta función lineal por pasos se define mediante los puntos de control de esta función, el intervalo de valores que la función puede convertir en y una operación opcional de ajuste de escala y desplazamiento que se puede aplicar después de la conversión. Una aplicación puede llamar al método [**IDXGIOutput:: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) para recuperar todas estas funcionalidades de control en la estructura de las [**\_ \_ \_ funciones de control gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) .

En este gráfico se muestra una función lineal con solo cuatro puntos de control.

![función lineal de corrección gamma](images/gamma-linear-function.png)

DXGI define los puntos de control por su ubicación a lo largo del eje de color de la superficie. En el gráfico anterior, las ubicaciones de los puntos de control son 0, 0,5, 0,75 y 1,0. Estos puntos de control indican que el hardware puede convertir valores en el intervalo de 0 a 1,0. DXGI enumera estos puntos de control en el miembro de matriz **ControlPointPositions** de las [**\_ \_ \_ capacidades de control gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) y siempre los declara en orden ascendente. DXGI solo rellena los primeros elementos de la matriz **ControlPointPositions** e indica el número de elementos con el miembro **NumGammaControlPoints** de las **\_ capacidades de \_ control \_ gamma de DXGI**. Si **NumGammaControlPoints** es menor que 1025, DXGI deja el resto de los elementos **ControlPointPositions** sin definir.

El hardware representado por este gráfico puede convertir valores en un intervalo de 0 a 1,25. Por lo tanto, DXGI establece los miembros **MinConvertedValue** y **MaxConvertedValue** en 0.0 f y 1,25 f respectivamente.

DXGI establece el miembro **ScaleAndOffsetSupported** de [**las \_ \_ \_ capacidades de control gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) para indicar si el hardware admite la capacidad de escalado y desplazamiento. Si el hardware admite la escala y el desplazamiento, mantiene una tabla de búsqueda de uno a uno simple, pero luego ajusta el resultado de la tabla para ajustar la salida a un intervalo mayor que \[ 0, 1 \] . El hardware primero escala los valores que salen de la tabla de búsqueda y, a continuación, los desplaza.

> [!Note]  
> Los distintos monitores conectados al mismo equipo pueden tener diferentes capacidades de control gamma. Además, las funciones de control gamma pueden cambiar de hecho en función del modo de presentación de la salida. Por lo tanto, se recomienda llamar siempre a [**IDXGIOutput:: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) para consultar las capacidades de control gamma después de que la aplicación entre en modo de pantalla completa.

 

Puede usar estos valores de capacidad de control gamma para derivar valores de control que después puede establecer mediante la API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

## <a name="setting-gamma-control-with-dxgi"></a>Establecer el control gamma con DXGI

Para establecer controles gamma, se pasa un puntero a una estructura de [**\_ \_ control gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) cuando se llama a la API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

Establezca los miembros de **escala** y **desplazamiento** de [**\_ \_ control gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) para especificar los valores de escala y desplazamiento que desea que el hardware aplique a los valores que obtiene de la tabla de búsqueda. Puede establecer la **escala** de forma segura en 1 y el **desplazamiento** en cero (es decir, una escala en uno no tiene ningún efecto y un desplazamiento de cero no tiene ningún efecto) si no desea usar la funcionalidad de escalado y desplazamiento, o si el hardware no tiene esa capacidad.

El miembro de la matriz **GammaCurve** del [**\_ \_ control gamma de dxgi**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) se establece en una lista de estructuras [**\_ RGB de dxgi**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) para los puntos de la curva gamma. Cada **elemento \_ RGB de DXGI** especifica los valores float que representan los componentes rojo, verde y azul para ese punto. La curva gamma no usa valores alfa. El número que ha obtenido de **NumGammaControlPoints** de las [**\_ \_ \_ funciones de control gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) se usa para rellenar el número de elementos de la matriz de **GammaCurve** . Cada elemento que se coloca en la matriz **GammaCurve** es el alto de cada punto de control.

Observe en el gráfico anterior que ahora tiene control sobre la posición vertical de cada punto de control y tiene control independiente para rojo, verde y azul. Por ejemplo, puede establecer todos los valores verdes y azules en cero y establecer los valores rojos en una escalera ascendente de cero a uno. En este escenario, la imagen mostrada muestra solo sus partes rojas, donde el azul y el verde aparecen como negro. También puede establecer una escalera descendente para todos los colores, lo que da como resultado una pantalla invertida. Cualquier valor que se coloque en la matriz **GammaCurve** debe estar incluido en los valores obtenidos de los miembros **MinConvertedValue** y **MaxConvertedValue** de las [**\_ capacidades de \_ control \_ gamma de DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)).

## <a name="gamma-control-practicalities"></a>Prácticas de control gamma

Los controles gamma de DXGI solo se aplican siempre que la aplicación esté en pantalla completa. Windows restaura el estado anterior de la pantalla cuando la aplicación se cierra o vuelve al modo de ventana. Pero Windows no restaura el estado de gamma de la aplicación si la aplicación vuelve a entrar en el modo de pantalla completa. La aplicación debe restaurar explícitamente su estado de gamma cuando vuelva a entrar en modo de pantalla completa.

No todos los adaptadores admiten el control gamma. Si un adaptador no admite el control gamma, omite las llamadas para establecer una rampa gamma.

Las aplicaciones que se ejecutan en escritorio remoto no pueden controlar gamma en absoluto.

El cursor del mouse, si se implementa en hardware (como la mayoría), normalmente no responde a la configuración gamma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
