---
description: Corrección gamma, o gamma para abre abrez, es el nombre de una operación no lineal que los sistemas usan para codificar y descodificar valores de píxeles en imágenes.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Uso de la corrección gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c940db1a94fb41e9babecbeb3075aa9e01b3732
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264444"
---
# <a name="using-gamma-correction"></a>Uso de la corrección gamma

Corrección gamma, o gamma para abre abrez, es el nombre de una operación no lineal que los sistemas usan para codificar y descodificar valores de píxeles en imágenes.

-   [¿Para qué es gamma y para qué se trata?](#what-is-gamma-and-what-is-it-for)
-   [Fondo de gamma en Windows](#background-of-gamma-on-windows)
-   [Evolución del hardware de presentación](#evolution-of-display-hardware)
-   [Funcionalidades de control gamma en DXGI](#gamma-control-capabilities-in-dxgi)
-   [Configuración del control gamma con DXGI](#setting-gamma-control-with-dxgi)
-   [Aspectos prácticos del control gamma](#gamma-control-practicalities)
-   [Temas relacionados](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>¿Para qué es gamma y para qué se trata?

Al final de la canalización de gráficos, justo donde la imagen sale del equipo para realizar su recorrido a lo largo del cable del monitor, hay un pequeño fragmento de hardware que puede transformar los valores de píxel sobre la marcha. Este hardware suele usar una tabla de búsqueda para transformar los píxeles. Este hardware usa los valores rojo, verde y azul que proceden de la superficie que se va a mostrar para buscar valores corregidos gamma en la tabla y, a continuación, envía los valores corregidos al monitor en lugar de los valores reales de la superficie. Por lo tanto, esta tabla de búsqueda es una oportunidad para reemplazar cualquier color por cualquier otro color. Aunque la tabla tiene ese nivel de potencia, el uso típico es ajustar las imágenes de forma sutil para compensar las diferencias en la respuesta del monitor. La respuesta del monitor es la función que relaciona el valor numérico de los componentes rojo, verde y azul de un píxel con el brillo mostrado de ese píxel.

Eso es para lo que se ha diseñado esta tabla, pero los desarrolladores de juegos encontraron usos creativos para ella, como el hecho de que toda la pantalla se parpadee en rojo para que su efecto sea beneficioso. En las aplicaciones de juego modernas, como parte del procesamiento posterior de cada fotograma, normalmente proporcionamos otras maneras de hacer estas cosas. De hecho, se recomienda dejar la tabla gamma sola porque podría estar en uso para calibrar la respuesta del monitor y los cambios mayoristas en la rampa gamma destruirán esta calibración cuidadosa.

La ciencia de determinar la corrección gamma es compleja y no se presenta aquí, aparte de para ilustrar de dónde provenía el nombre "gamma". La respuesta de un monitor CRT (es decir, un anteojo antiguo) es una función compleja, pero la física de estos monitores significa que muestran una respuesta que puede representarse de forma desa prueba mediante esta función de energía:

brightness( input ) = input<sup>gamma</sup>

El valor gamma suele estar cerca de un valor de 2,0. Los monitores DE LAC y todas las demás tecnologías más recientes están diseñados específicamente para presentar una respuesta similar, por lo que no es necesario volver a diseñar todo el software y las imágenes para esas nuevas tecnologías. El estándar sRGB declara que este valor gamma es exactamente 2,2 y este valor se ha convertido en un estándar ampliamente implementado.

El ojo humano también tiene una función de respuesta que invierte aproximadamente la función de energía crt. Esto significa que el brillo percibido de un píxel sube de forma muy lineal con los valores RGB de ese píxel.

Dado que un valor gamma de 2.2 se ha convertido en un estándar de facto, normalmente no es necesario preocuparnos demasiado por la curva gamma codificada en esta tabla y puede dejarlo como una asignación lineal uno a uno. Por supuesto, la coincidencia de colores adecuada requiere cuidado con esta función, pero esa discusión está fuera del ámbito de este tema. Windows incluye una herramienta que permite a los usuarios calibrar sus pantallas a gamma 2.2, y esta herramienta usa el hardware de la tabla de búsqueda para derivar un ajuste sutil cuidadosamente elegido para sus equipos. Los usuarios pueden ejecutar esta herramienta buscando "calibrar color". También hay perfiles de color bien definidos para determinados monitores que automatizan este proceso. La herramienta "calibrar color" puede detectar estos monitores más recientes e informar a los usuarios de que la calibración ya está en su lugar.

Esta noción de codificar una ley de energía en valores de color también es útil en otra parte de la canalización de gráficos, especialmente en texturas. En el caso de las texturas, quiere más precisión en los colores más oscuros debido a la respuesta logarítmica de los ojos humanos de la que se acaba de hablar. Es importante controlar cuidadosamente gamma en esta parte de la canalización. Para obtener más información, [vea Conversión de datos para el espacio de colores.](converting-data-color-space.md)

El resto de este tema se centra solo en la corrección gamma en esta última parte de la canalización, entre los datos del búfer de fotogramas y el monitor. Si desea escribir un asistente de calibración o crear efectos especiales en una aplicación de pantalla completa en la que un paso posterior al procesamiento no es práctico, esta es la información que necesita.

## <a name="background-of-gamma-on-windows"></a>Fondo de gamma en Windows

Windows equipos suelen tener una tabla gamma que es una tabla de búsqueda que toma un triple de bytes y genera un triple de bytes. Estos tripletes son 768 (256 x 3) bytes de RAM. Esto es correcto cuando el formato de presentación contiene un triplete de valores BYTE RGB, pero no es lo suficientemente expresivo como para describir las transformaciones que puede desear cuando el formato de presentación tiene un intervalo mayor que 0,1, como los valores de punto \[ \] flotante. Las API de Windows control gamma han seguido una evolución a medida que los formatos de presentación se han vuelto más complejos.

Las primeras WINDOWS api que ofrecen el control gamma son [**setDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) de Windows Interfaz de dispositivo gráfico (GDI) y [**GetDeviceGammaRamp.**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp) Estas API funcionan con tres matrices de 256 entradas de WORD, con cada codificación WORD cero hasta una, representadas por los valores de WORD 0 y 65535. La precisión adicional de una palabra normalmente no está disponible en las tablas de búsqueda de hardware reales, pero estas API estaban diseñadas para ser flexibles. Estas API, a diferencia de las otras descritas más adelante en esta sección, solo permiten una pequeña desviación de una función de identidad. De hecho, cualquier entrada de la rampa debe estar dentro del 32768 del valor de identidad. Esta restricción significa que ninguna aplicación puede convertir la pantalla en completamente negra o en algún otro color ilegible.

La siguiente API es [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)de Microsoft Direct3D 9, que sigue el mismo patrón y formato de datos que [**SetDeviceGammaRamp.**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) El valor predeterminado de la rampa gamma de Direct3D 9 no es especialmente útil; es una rampa de WORD inicializada en 0-255, no en 0-65535, aunque la API se defina en términos de 0-65535.

La API más reciente [**es IDXGIOutput::SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol). Esta API tiene un esquema más flexible para expresar el control gamma, ya que se adapta al mayor conjunto de formatos de presentación de DXGI, incluidos diez bits enteros por canal, formatos float de 16 bits y el formato de intervalo extendido \_ XR BIAS.

Todas estas API funcionan en el mismo hardware y cambian los mismos valores. Las API de Direct3D 9 y DXGI son de "solo escritura". No se puede leer el valor del hardware, modificarlo y, a continuación, establecerlo. Solo puede establecer la rampa. Además, solo puede establecer gamma cuando la aplicación está a pantalla completa. Esta restricción es otra manera de garantizar que el escritorio siempre es legible. Es decir, la aplicación puede alterar su propia pantalla, pero Windows restaurará la rampa gamma anterior cuando la aplicación pierda pantalla completa (por ejemplo, a través de alt-tab o ctrl-alt-supr).

## <a name="evolution-of-display-hardware"></a>Evolución del hardware de presentación

Algunos monitores más recientes pueden mostrar una amplia gama detenciones. Sin embargo, cuando el formato de presentación solo puede representar valores entre cero y uno, la pantalla debe asignar cero a su valor más oscuro y uno a su valor más brillante. Este valor más brillante puede ser demasiado brillante para una visualización cómoda de páginas web con texto negro sobre un fondo blanco, pero es fantástico para efectos especiales sobresaltos, como ver la vista de un lago o un rayo forzándose el cielo. Por lo tanto, necesitamos una manera de expresar estos intervalos más amplios. DXGI 1.1 y versiones posteriores contiene valores de formato de presentación que permiten que 1.0 represente un valor blanco cómodo y reserva valores de formato de presentación más amplios para efectos especiales sobre-brillantes. DXGI 1.1 admite dos formatos de presentación que pueden expresar estos valores más amplios: DXGI \_ FORMAT \_ R10G10B10 XR BIAS A2 UNORM y punto flotante de \_ \_ \_ \_ 16 bits. Para obtener una explicación completa de estos formatos, vea [Detalles del formato extendido.](/windows-hardware/drivers/display/details-of-the-extended-format) A continuación, se verá por qué la API gamma [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) de DXGI necesita valores de píxel mayores que 1.0.

## <a name="gamma-control-capabilities-in-dxgi"></a>Funcionalidades de control gamma en DXGI

DXGI permite al controlador de pantalla expresar sus controles gamma como una función lineal paso a paso. Esta función lineal paso a paso se define mediante los puntos de control de esta función, el intervalo de valores a los que se puede convertir la función y una operación de escalado y desplazamiento opcional adicional que se puede aplicar después de la conversión. Una aplicación puede llamar al método [**IDXGIOutput::GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) para recuperar todas estas funcionalidades de control en la estructura [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES.**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))

Este gráfico muestra una función lineal con solo cuatro puntos de control.

![Función lineal de corrección gamma](images/gamma-linear-function.png)

DXGI define los puntos de control por su ubicación a lo largo del eje de color de la superficie. En el gráfico anterior, las ubicaciones de los puntos de control son 0, 0,5, 0,75 y 1,0. Estos puntos de control indican que el hardware puede convertir valores en el intervalo de 0 a 1,0. DXGI enumera estos puntos de control en el miembro de la matriz **ControlPointPositions** de [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) y los declara siempre en orden creciente. DXGI rellena solo los primeros elementos de la matriz **ControlPointPositions** e indica el número de elementos con el miembro **NumGammaControlPoints** de **DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**. Si **NumGammaControlPoints** es menor que 1025, DXGI deja sin definir el resto de los elementos **ControlPointPositions.**

El hardware representado por este gráfico puede convertir valores en un intervalo de 0 a 1,25. Por lo tanto, DXGI establece los **miembros MinConvertedValue** y **MaxConvertedValue** en 0,0f y 1,25f respectivamente.

DXGI establece el **miembro ScaleAndOffsetSupported** de [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) para indicar si el hardware admite la funcionalidad de escalado y desplazamiento. Si el hardware admite escalado y desplazamiento, mantiene una tabla de búsqueda uno a uno simple, pero ajusta la salida de la tabla para ajustar la salida a un intervalo mayor que \[ 0,1 \] . El hardware escala primero los valores que proceden de la tabla de búsqueda y, a continuación, los desplaza.

> [!Note]  
> Los distintos monitores conectados al mismo equipo pueden tener diferentes funcionalidades de control gamma. Además, las funcionalidades de control gamma pueden cambiar en función del modo de presentación de la salida. Por lo tanto, se recomienda llamar siempre a [**IDXGIOutput::GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) para consultar las funcionalidades de control gamma después de que la aplicación entre en modo de pantalla completa.

 

Puede usar estos valores de funcionalidad de control gamma para derivar valores de control que luego puede establecer mediante la API [**IDXGIOutput::SetGammaControl.**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol)

## <a name="setting-gamma-control-with-dxgi"></a>Configuración del control gamma con DXGI

Para establecer controles gamma, se pasa un puntero a una estructura [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) al llamar a la API [**IDXGIOutput::SetGammaControl.**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol)

Establezca los miembros **Scale** y **Offset** de [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) para especificar los valores de escala y desplazamiento que desea que el hardware aplique a los valores que se obtienen de la tabla de búsqueda. Puede establecer  Escala en 1 y Desplazamiento en cero (es decir, una escala por uno no tiene ningún efecto y un desplazamiento de cero no tiene ningún efecto) si no desea usar la funcionalidad de escalado y desplazamiento o si el hardware no tiene esa funcionalidad. 

Establezca el miembro **de la matriz GammaCurve** de [**DXGI GAMMA \_ \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) en una lista de estructuras [**RGB \_ DE DXGI**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) para los puntos de la curva gamma. Cada **elemento \_ RGB DXGI** especifica los valores float que representan los componentes rojo, verde y azul para ese punto. La curva gamma no usa valores alfa. Use el número que obtuvo de **NumGammaControlPoints** de [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) para rellenar ese número de elementos en la **matriz GammaCurve.** Cada elemento que se coloca en la **matriz GammaCurve** es el alto de cada punto de control.

Observe en el gráfico anterior que ahora tiene control sobre la posición vertical de cada punto de control y tiene un control independiente para rojo, verde y azul. Por ejemplo, puede establecer todos los valores de verde y azul en cero y establecer los valores rojos en un orden ascendente de cero a uno. En este escenario, la imagen mostrada muestra solo sus partes de color rojo, donde el azul y el verde aparecen como negro. También puede establecer una degradación descendente para todos los colores, lo que da como resultado una presentación invertida. Cualquier valor que coloque en la **matriz GammaCurve** debe estar incluido dentro de los valores obtenidos de los **miembros MinConvertedValue** y **MaxConvertedValue** de [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)).

## <a name="gamma-control-practicalities"></a>Aspectos prácticos del control gamma

Los controles gamma de DXGI solo se aplican siempre que la aplicación sea de pantalla completa. Windows restaura el estado anterior de la pantalla cuando la aplicación sale o vuelve al modo de ventana. Pero Windows no restaura el estado gamma de la aplicación si la aplicación vuelve a entrar en modo de pantalla completa. La aplicación debe restaurar explícitamente su estado gamma cuando vuelva a entrar en modo de pantalla completa.

No todos los adaptadores admiten el control gamma. Si un adaptador no admite el control gamma, omite las llamadas para establecer una rampa gamma.

Las aplicaciones que se ejecutan en escritorio remoto no pueden controlar gamma en absoluto.

El cursor del mouse, si se implementa en hardware (como la mayoría de los casos), normalmente no responde a la configuración gamma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
