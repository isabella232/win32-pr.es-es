---
description: Establecer propiedades en orígenes
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Establecer propiedades en orígenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de58e25cc9fdec34ed285ebbfc2e9cfd3dcdf95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906294"
---
# <a name="setting-properties-on-sources"></a>Establecer propiedades en orígenes

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Al crear un nuevo objeto de origen, hay algunas propiedades que se deben establecer y otras que se pueden establecer de forma opcional. Debe establecer las siguientes propiedades.

-   Horas de inicio y detención, relativas al resto de la escala de tiempo. Llame al método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) . No establezca tiempos de superposición en objetos de origen dentro de la misma pista o producirá un comportamiento no definido.
-   El archivo multimedia que se va a usar como clip de origen. Llame a [**IAMTimelineSrc:: SetMediaName**](iamtimelinesrc-setmedianame.md).
-   Horas de inicio y detención del medio, en relación con el archivo de código fuente original. Llame al método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Excepción: Si el origen es una imagen fija, no especifique las horas de los medios. Para obtener más información sobre las horas de los medios, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Un objeto de origen hereda su tipo de medio del grupo primario, por lo que no es necesario especificar un tipo de medio.

Entre las propiedades opcionales se incluyen las siguientes:

-   Modo de ajuste. El modo Stretch especifica cómo Microsoft® DirectShow® Editation Services (DES) representa un origen cuyo tamaño no coincide con las dimensiones de salida. De forma predeterminada, DES estira una imagen sin conservar la relación de aspecto. Como alternativa, DES puede recortar una imagen o crear una panorámica. Llame al método [**IAMTimelineSrc:: SetStretchMode**](iamtimelinesrc-setstretchmode.md) para especificar el modo Stretch.
-   La duración del archivo de código fuente. Si establece esta propiedad antes de establecer las horas del medio, DES valida la hora de detención del medio y trunca la hora de detención si supera la duración del archivo. Esto puede ayudar a evitar la representación de errores más adelante. Puede obtener la duración del archivo mediante el detector de medios, como se describe en [uso del detector de medios](using-the-media-detector.md). Llame al método [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md) para especificar la duración del archivo.
-   El número de secuencia. De forma predeterminada, un objeto de origen usa la primera secuencia del archivo que coincide con el tipo de medio del grupo primario. Si un archivo contiene dos o más secuencias del mismo tipo de medio, seleccione la secuencia que se va a usar mediante una llamada a [**IAMTimelineSrc:: SetStreamNumber**](iamtimelinesrc-setstreamnumber.md). Puede usar el detector de medios para buscar el número de flujos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



