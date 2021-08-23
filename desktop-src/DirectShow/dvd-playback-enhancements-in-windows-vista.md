---
description: Mejoras de reproducción de DVD en Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Mejoras de reproducción de DVD en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5757f5dd73dc547ae123490fd8de84b0606d1ade8490c9600486df0b846541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148718"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Mejoras de reproducción de DVD en Windows Vista

En esta sección se describen las mejoras en la reproducción y navegación de DVD Windows Vista.

**Especificar un descodificador**

En versiones anteriores de DirectShow, era difícil especificar un descodificador MPEG-2 determinado al crear un gráfico de reproducción de DVD. A partir Windows Vista, una aplicación puede especificar el descodificador de la siguiente manera:

1.  Agregue el descodificador al gráfico antes de llamar a [**IDvdGraphBuilder::RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Llame **a RenderDvdVideoVolume y** establezca la marca NO BORRAR DEL DVD DE \_ \_ \_ \_ AM. El navegador de DVD dará preferencia al descodificador que agregó.

**Compatibilidad con el representador de vídeo mejorado**

Se recomienda que las aplicaciones escritas para Windows Vista o versiones posteriores usen [**el representador**](enhanced-video-renderer-filter.md) de vídeo mejorado (EVR) para la reproducción de vídeo. Para usar evr en una aplicación de reproducción de DVD, establezca la marca AM DVD EVR ONLY al llamar a \_ \_ \_ **RenderDvdVideoVolume**.

Para configurar la EVR antes de compilar el gráfico, llame a [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) y consulte la **interfaz IEVRFilterConfig** o **IMFVideoRenderer.** (Estas interfaces se documentan en la documentación Media Foundation SDK). Para obtener más información sobre cómo configurar el representador de vídeo en un gráfico de reproducción de DVD, vea [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

El navegador de DVD no usará el EVR a menos que el método [**IAMDecoderCaps::GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) del descodificador devuelva la marca DE COMPATIBILIDAD DE AM \_ GETDECODERCAP \_ QUERY \_ \_ EVR. Esta marca se define para asegurarse de que las aplicaciones son compatibles con los descodificadores existentes. Si **RenderDvdVideoVolume** produce un error al usar la marca EVR ONLY del DVD de AM, vuelva a otro representador de vídeo llamando al método de nuevo \_ sin la marca \_ \_ .

**Reproducción inversa sin problemas**

El navegador de DVD ahora puede realizar una reproducción inversa sin problemas. En una reproducción inversa sin problemas, el navegador de DVD envía unidades de objeto de vídeo (VOB) enteras al descodificador y el descodificador emite los fotogramas en orden inverso. Esta característica requiere que los descodificadores admitan una reproducción inversa sin problemas.

Cuando la aplicación establece la velocidad de reproducción en un valor negativo, el navegador de DVD consulta a los descodificadores la propiedad [**\_ \_ ReverseMaxFullDataRate**](am-rate-reversemaxfulldatarate-property.md) de AM RATE. El valor de esta propiedad es el valor absoluto de la velocidad inversa máxima x 10000. Por ejemplo, si la velocidad inversa máxima es -2,0, el valor es 20000.

Si el descodificador de vídeo admite la propiedad , el navegador de DVD usa una reproducción inversa sin problemas. La secuencia de audio se reproduce en orden inverso si el descodificador de audio admite la propiedad ; De lo contrario, la secuencia de audio se silencia. Si el descodificador de vídeo no admite la propiedad o la velocidad de reproducción supera la velocidad inversa máxima del descodificador de vídeo, el navegador de DVD cambia al *modo de examen*. En el modo de examen, el navegador de DVD envía solo fotogramas I al descodificador y quita todos los fotogramas B y P.

Durante la reproducción inversa sin problemas, el navegador de DVD envía VOBUs completas al descodificador. El navegador de DVD envía las VOB En orden inverso, pero envía los fotogramas dentro de cada VOBU en su orden de avance normal. Al principio de cada VOBU, el navegador de DVD establece la marca \_ ReverseBlockStart de AM en el ejemplo. Al final de VOBU, el navegador de DVD envía un ejemplo vacío con la \_ marca ReverseBlockEnd de AM. Para recuperar estas marcas, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. Las marcas se establecen en el **miembro dwTypeSpecificFlags** de la [**estructura PROPERTIES DE AM \_ SAMPLE2. \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

El descodificador almacena en caché los datos de vídeo hasta que recibe el ejemplo con la \_ marca ReverseBlockEnd de AM. En ese momento, el descodificador entrega fotogramas descodificados en orden inverso. Por ejemplo, si VOBU 1 contiene fotogramas 1-4 y VOBU 2 contiene fotogramas de 5 a 8, el navegador de DVD enviará los fotogramas en este orden:

(Inicio del bloque) F5 F6 F7 F8 (final de bloque) (inicio de bloque) F1 F2 F3 F4 (extremo de bloque)

El descodificador debe procesar los fotogramas de la manera siguiente:

1.  Descodificar VOBU 2.
2.  Marcos de salida: F8 F7 F6 F5
3.  Descodificar VOBU 1.
4.  Marcos de salida: F4 F3 F2 F1

El navegador de DVD establece la marca de tiempo en el primer ejemplo de VOBU (F1 y F5 en este ejemplo), pero la marca de tiempo contiene la hora de presentación del inicio del bloque, por lo que el descodificador debe aplicar esta hora a la última muestra del bloque (F4 y F8). Los tiempos de presentación aumentan durante la reproducción inversa.

Normalmente, una VOBU contiene hasta 42 fotogramas y puede contener más de un grupo de imágenes (GOP). Para habilitar la descodificación completa de VOBU, el descodificador debe almacenar en caché los fotogramas I y P descodificados. Las VOBus en DVD no son GOP cerradas, por lo que un fotograma B dentro de un GOP puede requerir la descodación de todos los fotogramas de referencia del GOP anterior. Si el descodificador no tiene suficientes superficies para contener todos los fotogramas descodificados, es posible que tenga que volver a descodificar los fotogramas seleccionados.

**Cambios de velocidad**

De forma predeterminada, el navegador de DVD vacía el gráfico entre los cambios de velocidad. Sin embargo, si el descodificador admite la propiedad [**\_ \_ ResetOnTimeDisc**](am-rate-resetontimedisc-property.md) de AM RATE, el navegador de DVD no vaciará el gráfico, lo que dará lugar a una transición más fluida entre las velocidades de reproducción.

El navegador de DVD siempre marca las marcas de tiempo para la reproducción a una velocidad de 1x, independientemente de la velocidad de reproducción real. El descodificador debe escalar las marcas de tiempo en las muestras descodificadas para que coincidan con la velocidad de reproducción real. (Para obtener más información, [**vea Propiedad \_ \_ SimpleRateChange de AM RATE).**](am-rate-simpleratechange-property.md) Como resultado, al reproducir a velocidades diferentes de 1x, las marcas de tiempo de los fotogramas descodificados difieren de las de los fotogramas codificados. Cada vez que el navegador de DVD establece la marca AM SAMPLE TIMEDISCONTINUITY en un ejemplo, el descodificador debe \_ \_ resincronizar sus marcas de tiempo. En otras palabras, el marco descodificado debe tener la misma marca de tiempo que el marco de entrada. Para recuperar la marca \_ AM SAMPLE \_ TIMEDISCONTINUITY, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. La marca se establece en el **miembro dwSampleFlags** de la [**estructura PROPIEDADES DE AM \_ \_ SAMPLE2.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

**Administración de energía**

En Windows Vista, el navegador de DVD permite las siguientes mejoras en la administración de energía:

-   Mayor resolución del temporizador
-   Caché de datos más grande

**Resolución de temporizador:** las aplicaciones pueden solicitar una resolución de temporizador mínima llamando a la **función timeBeginPeriod.** Una resolución mayor (período más corto) aumenta la capacidad de respuesta del sistema a eventos periódicos, como tiempos de espera, pero también puede aumentar la frecuencia de los cambios de contexto del subproceso.

De forma predeterminada, el reloj de referencia DirectShow establece la resolución del temporizador en 1 milisegundo. En esa resolución, la CPU no entrará en ningún modo de ahorro de energía. A partir de Windows Vista, el navegador de DVD invalida el comportamiento predeterminado del reloj de referencia llamando a [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) en el reloj de referencia. Esto quita la solicitud del reloj para una resolución de temporizador de 1 milisegundo. Esto podría permitir que la CPU entre en un modo de ahorro de energía.

La resolución de temporizador es una configuración global; Windows elige el valor más bajo solicitado. Los filtros de representador de mezcla de vídeo (VMR) (VMR-7 y VMR-9) establecen la resolución del temporizador en 1 milisegundo. Normalmente, el EVR establece la resolución en un valor entre 4 y 8 milisegundos, dependiendo de si la composición del escritorio está habilitada y de si la EVR está en modo de pantalla completa. Otras aplicaciones también pueden establecer la resolución.

**Tamaño de caché:** las aplicaciones pueden especificar la cantidad de datos que almacena en caché el navegador de DVD estableciendo la opción DVD CacheSizeInMB en el \_ método [**IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) Si la aplicación establece esta marca en un valor grande (> 50 MB), la unidad de DVD puede girar después de la captura previa inicial, dependiendo del hardware, lo que puede reducir el consumo de energía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



