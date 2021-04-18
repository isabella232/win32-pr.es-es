---
description: Flujos opcionales
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Flujos opcionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686313"
---
# <a name="optional-streams"></a>Flujos opcionales

Un DMO puede designar algunos de sus flujos de salida como opcionales. Un flujo opcional genera datos que la aplicación puede descartar, ya sea por completo o en muestras ocasionales. Por ejemplo, un flujo opcional podría contener información adicional sobre una secuencia principal.

Para consultar si una secuencia es opcional, llame al método [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) y compruebe el parámetro *pdwFlags* . Las secuencias opcionales devuelven la \_ marca de salida DMO \_ STREAMF \_ descartable o la \_ marca de salida DMO \_ STREAMF \_ opcional. Estas marcas significan casi lo mismo: una diferencia menor entre ellas se explicará en breve.

Si una secuencia es opcional, el cliente puede indicar a DMO que descarte los datos de esa secuencia cuando procesa la salida. Para ello, llame al método [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) y establezca el búfer de salida en **null** para cada flujo que desee descartar. (El búfer de salida se especifica en el miembro **pBuffer** del [**\_ búfer de \_ datos \_ de salida de DMO**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer)). Establezca también la salida del proceso de DMO \_ \_ \_ descartada \_ cuando \_ no haya ninguna \_ marca de búfer en el parámetro *dwFlags* .

Para cada flujo en el que el puntero *pBuffer* sea **null**, DMO intentará descartar los datos. Si la secuencia es opcional, se garantiza que la DMO descarta los datos. Si la secuencia no es opcional, DMO descarta los datos cuando sea posible, pero no se garantiza que lo haga. Si no puede descartar los datos, establece la \_ marca de datos de salida DMO \_ \_ BUFFERF \_ incompleta. Si establece un puntero de *pBuffer* en **null** pero no establece la salida del proceso de DMO en \_ \_ \_ descartar \_ cuando \_ no hay ninguna \_ marca de búfer, DMO no descarta los datos. En ese caso, DMO almacena en búfer el resultado internamente o simplemente produce un error en la llamada a **ProcessOutput** .

La única diferencia funcional entre la \_ marca opcional STREAMF de salida de DMO \_ \_ y la marca de salida de DMO \_ \_ STREAMF \_ se indica a continuación:

-   La \_ marca de salida DMO \_ STREAMF \_ opcional indica que el cliente no tiene que establecer un tipo de medio en esa secuencia. Sin embargo, si el cliente comienza a procesar datos sin establecer el tipo de medio para la secuencia, debe descartar los datos de esa secuencia durante toda la duración de la transmisión por secuencias. Si desea descartar ejemplos de forma selectiva, debe establecer el tipo de medio.
-   La marca de salida de DMO \_ \_ STREAMF \_ descartable indica que, aunque la secuencia es opcional, siempre requiere un tipo de medio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedar directamente un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



