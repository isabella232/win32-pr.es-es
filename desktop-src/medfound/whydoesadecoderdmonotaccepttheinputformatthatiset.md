---
description: ¿Por qué un descodificador no acepta el formato de entrada que configuro?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: ¿Por qué un descodificador no acepta el formato de entrada que configuro?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696857"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>¿Por qué un descodificador no acepta el formato de entrada que configuro?

Hay muchas razones por las que un descodificador podría rechazar un formato. Los datos de formato extendido más comunes faltan o son incorrectos. Los datos de formato extendido son información específica del códec que se anexa a la estructura que describe el tipo de medio.

Cuando se enumera un tipo de salida mediante un objeto de codificador, el miembro **pbFormat** de la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) apuntará a una estructura **WAVEFORMATEX** . Esta estructura tiene datos de formato extendido anexados y el tamaño de los datos se almacena en el miembro **WAVEFORMATEX. cbSize** . Independientemente del contenedor utilizado para almacenar los datos comprimidos, debe conservar la estructura **WAVEFORMATEX** y usarlo en el tipo de entrada para el descodificador. Sin los datos de formato extendido, el descodificador no puede descomprimir el contenido.

En el caso de los formatos de vídeo, debe recuperar manualmente los datos de formato extendido y anexarlos a la estructura **VIDEOINFOHEADER** . Para obtener más información, consulte [uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 
