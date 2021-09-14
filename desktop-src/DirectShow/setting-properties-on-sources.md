---
description: Establecer propiedades en orígenes
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Establecer propiedades en orígenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de58e25cc9fdec34ed285ebbfc2e9cfd3dcdf95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061594"
---
# <a name="setting-properties-on-sources"></a>Establecer propiedades en orígenes

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Al crear un nuevo objeto de origen, hay algunas propiedades que debe establecer y otras que, opcionalmente, puede establecer. Debe establecer las siguientes propiedades.

-   Las horas de inicio y de detenerse, en relación con el resto de la escala de tiempo. Llame al [**método IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md) No establezca horas superpuestas en objetos de origen dentro de la misma pista o provocará un comportamiento indefinido.
-   Archivo multimedia que se usará como clip de origen. Llame a [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md).
-   Las horas de inicio y de detenerse del medio, en relación con el archivo de código fuente original. Llame al [**método IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Excepción: si el origen es una imagen fija, no especifique las horas del medio. Para obtener más información sobre los tiempos multimedia, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Un objeto de origen hereda su tipo de medio del grupo primario, por lo que no es necesario especificar un tipo de medio.

Entre las propiedades opcionales se incluyen las siguientes:

-   Modo de ajuste. El modo de ajuste especifica cómo Microsoft® DirectShow® Editing Services (DES) representa un origen cuyo tamaño no coincide con las dimensiones de salida. De forma predeterminada, DES extiende una imagen sin conservar la relación de aspecto. Como alternativa, DES puede recortar una imagen o crear un cuadro de texto. Llame al [**método IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md) para especificar el modo stretch.
-   Duración del archivo de origen. Si establece esta propiedad antes de establecer las horas del medio, DES valida el tiempo de detenerse del medio y trunca la hora de detenerse si supera la duración del archivo. Esto puede ayudar a evitar errores de representación más adelante. Puede obtener la duración del archivo mediante el detector de medios, como se describe en [Uso del detector de medios](using-the-media-detector.md). Llame al [**método IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md) para especificar la duración del archivo.
-   Número de secuencia. De forma predeterminada, un objeto de origen usa la primera secuencia del archivo que coincide con el tipo de medio del grupo primario. Si un archivo contiene dos o más secuencias del mismo tipo de medio, seleccione la secuencia que se va a usar llamando a [**IAMTimelineSrc::SetStreamNumber.**](iamtimelinesrc-setstreamnumber.md) Puede usar el detector de medios para encontrar el número de secuencias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



