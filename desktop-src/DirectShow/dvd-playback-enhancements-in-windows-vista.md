---
description: Mejoras en la reproducción de DVD en Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Mejoras en la reproducción de DVD en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159056d2c7acaec18a73a30b21f79bcd6267ca33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652317"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Mejoras en la reproducción de DVD en Windows Vista

En esta sección se describen las mejoras en la reproducción y la navegación por DVD en Windows Vista.

**Especificar un descodificador**

En versiones anteriores de DirectShow, era difícil especificar un descodificador MPEG-2 determinado al crear un gráfico de reproducción de DVD. A partir de Windows Vista, una aplicación puede especificar el descodificador como se indica a continuación:

1.  Agregue el descodificador al gráfico antes de llamar a [**IDvdGraphBuilder:: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Llame a **RenderDvdVideoVolume** y establezca la \_ marca AM DVD \_ \_ no \_ Clear. El navegador de DVD dará preferencia al descodificador que ha agregado.

**Compatibilidad con el representador de vídeo mejorado**

Se recomienda que las aplicaciones escritas para Windows Vista o posterior usen el [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR) para la reproducción de vídeo. Para usar EVR en una aplicación de reproducción de DVD, establezca la \_ marca AM DVD \_ EVR \_ Only al llamar a **RenderDvdVideoVolume**.

Para configurar el EVR antes de compilar el gráfico, llame a [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) y consulte la interfaz **IEVRFilterConfig** o **IMFVideoRenderer** . (Estas interfaces se documentan en la documentación del SDK de Media Foundation). Para obtener más información acerca de cómo configurar el representador de vídeo en un gráfico de reproducción de DVD, consulte [crear el gráfico de filtros de DVD](building-the-dvd-filter-graph.md).

El navegador de DVD no usará EVR a menos que el método [**IAMDecoderCaps:: GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) del descodificador devuelva \_ la \_ \_ marca de soporte técnico EVR de consulta AM GETDECODERCAP \_ . Esta marca se define para garantizar que las aplicaciones son compatibles con los descodificadores existentes. Si se produce un error en **RenderDvdVideoVolume** con la marca AM de \_ DVD \_ EVR \_ Only, revierta a otro representador de vídeo llamando al método de nuevo sin la marca.

**Reproducción inversa suave**

El navegador de DVD ahora puede realizar una reproducción de Smooth inverso. En la reproducción Smooth inverso, el navegador de DVD envía unidades de objeto de vídeo (VOBUs) completas al descodificador y el descodificador emite los fotogramas en orden inverso. Esta característica requiere que los descodificadores admitan la reproducción de Smooth inverso.

Cuando la aplicación establece la velocidad de reproducción en un valor negativo, el navegador de DVD consulta los descodificadores de la propiedad [**\_ \_ ReverseMaxFullDataRate Rate**](am-rate-reversemaxfulldatarate-property.md) . El valor de esta propiedad es el valor absoluto de la velocidad máxima inversa x 10000. Por ejemplo, si la velocidad máxima inversa es-2,0, el valor es 20000.

Si el descodificador de vídeo admite la propiedad, el navegador de DVD utiliza la reproducción fluida. La secuencia de audio se reproduce en orden inverso si el descodificador de audio admite la propiedad; de lo contrario, se silencia la secuencia de audio. Si el descodificador de vídeo no admite la propiedad, o si la velocidad de reproducción supera la tasa de reversión máxima del descodificador de vídeo, el navegador de DVD cambia al *modo de exploración*. En el modo de exploración, el navegador de DVD envía solo I fotogramas al descodificador y quita todos los fotogramas B y P.

Durante la reproducción de Smooth inverso, el navegador de DVD envía VOBUs completos al descodificador. El navegador de DVD envía el VOBUs en orden inverso, pero envía los fotogramas dentro de cada VOBU en su orden de avance normal. Al principio de cada VOBU, el navegador de DVD establece la \_ marca AM ReverseBlockStart en el ejemplo. Al final de la VOBU, el navegador de DVD envía un ejemplo vacío con la \_ marca AM ReverseBlockEnd. Para recuperar estas marcas, llame a [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. Las marcas se establecen en el miembro **dwTypeSpecificFlags** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

El descodificador almacena en caché los datos de vídeo hasta que recibe el ejemplo con la \_ marca AM ReverseBlockEnd. En ese momento, el descodificador entrega los fotogramas descodificados en orden inverso. Por ejemplo, si VOBU 1 contiene los fotogramas 1 – 4 y VOBU 2 contiene los fotogramas 5 – 8, el navegador de DVD enviará los fotogramas en este orden:

(Inicio de bloque) F5 F6 F7 F8 (fin de bloque) (inicio de bloque) F1 F2 F3 F4 (fin de bloque)

El descodificador debe procesar los fotogramas de la manera siguiente:

1.  Descodifique VOBU 2.
2.  Fotogramas de salida: F8 F7 F6 F5
3.  Descodificación de VOBU 1.
4.  Fotogramas de salida: F4 F3 F2 F1

El navegador de DVD establece la marca de tiempo en el primer ejemplo de VOBU (F1 y F5 en este ejemplo), pero la marca de tiempo contiene el tiempo de presentación del inicio del bloque, por lo que el descodificador debería aplicar esta vez a la última muestra del bloque (F4 y F8). Los tiempos de presentación aumentan durante la reproducción inversa.

Normalmente, un VOBU contiene hasta 42 fotogramas y puede contener más de un grupo de imágenes (GOP). Para permitir descodificar el VOBU completo, el descodificador debe almacenar en caché los fotogramas I y P descodificados. VOBUs en DVDs no están cerrados GOP, por lo que una trama B dentro de un GOP puede requerir la descodificación de todos los fotogramas de referencia del GOP anterior. Si el descodificador no tiene suficientes superficies para contener todos los fotogramas descodificados, es posible que tenga que volver a descodificar los fotogramas seleccionados.

**Cambiar velocidad**

De forma predeterminada, el navegador de DVD vacía el gráfico entre los cambios de velocidad. Sin embargo, si el descodificador es compatible con la propiedad [**\_ \_ ResetOnTimeDisc Rate**](am-rate-resetontimedisc-property.md) , el explorador de DVD no vaciará el gráfico, lo que dará lugar a una transición más suave entre las velocidades de reproducción.

El explorador de DVD siempre muestra las marcas de tiempo para la reproducción a la velocidad de 1x, independientemente de la velocidad de reproducción real. El descodificador debe escalar las marcas de tiempo en los ejemplos descodificados para que coincidan con la velocidad de reproducción real. (Para obtener más información, consulte la [**\_ propiedad tasa AM \_ SimpleRateChange**](am-rate-simpleratechange-property.md)). Como resultado, al reproducirse a velocidades distintas de 1x, las marcas de tiempo de los fotogramas descodificados difieren de las de los fotogramas codificados. Siempre que el navegador de DVD establezca \_ la \_ marca AM de ejemplo TIMEDISCONTINUITY en un ejemplo, el descodificador debe volver a sincronizar sus marcas de tiempo. En otras palabras, el marco descodificado debe tener la misma marca de tiempo que el marco de entrada. Para recuperar la \_ marca TIMEDISCONTINUITY de ejemplo AM \_ , llame a [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo. La marca se establece en el miembro **dwSampleFlags** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

**Administración de energía**

En Windows Vista, el explorador de DVD permite las siguientes mejoras en la administración de energía:

-   Mayor resolución del temporizador
-   Caché de datos más grande

**Resolución del temporizador**: las aplicaciones pueden solicitar una resolución de temporizador mínima llamando a la función **timeBeginPeriod** . Una resolución más alta (período más corto) aumenta la capacidad de respuesta del sistema a eventos periódicos, como los tiempos de espera, pero también puede aumentar la frecuencia de los cambios de contexto de subproceso.

De forma predeterminada, el reloj de referencia de DirectShow establece la resolución del temporizador en 1 milisegundo. En esa resolución, la CPU no entrará en ningún modo de ahorro de energía. A partir de Windows Vista, el explorador de DVD invalida el comportamiento predeterminado del reloj de referencia mediante una llamada a [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) en el reloj de referencia. Esto quita la solicitud del reloj para una resolución de temporizador de 1 milisegundo. Esto podría permitir que la CPU entrara en modo de ahorro de energía.

La resolución del temporizador es una configuración global; Windows elige el valor solicitado más bajo. Los filtros de representador de mezcla de vídeo (VMR) (VMR-7 y VMR-9) establecen la resolución del temporizador en 1 milisegundo. Normalmente, EVR establece la resolución en un valor entre 4 y 8 milisegundos, dependiendo de si la composición de escritorio está habilitada y si el valor de EVR está en modo de pantalla completa. Otras aplicaciones también pueden establecer la resolución.

**Tamaño de caché**: las aplicaciones pueden especificar la cantidad de datos que almacena en caché el navegador de DVD mediante la configuración de la \_ opción de DVD CacheSizeInMB en el método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) . Si la aplicación establece esta marca en un valor grande (> 50 MB), la unidad de DVD puede reducirse después de la captura previa inicial, en función del hardware, lo que puede reducir el consumo de energía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



