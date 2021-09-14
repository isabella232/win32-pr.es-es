---
description: ¿Por qué un descodificador no acepta el formato de entrada que he establecido?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: ¿Por qué un descodificador no acepta el formato de entrada que he establecido?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263156"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>¿Por qué un descodificador no acepta el formato de entrada que he establecido?

Hay muchas razones por las que un descodificador podría rechazar un formato. Lo más común son los datos de formato extendido que faltan o son incorrectos. Los datos de formato extendido son información específica del códec que se anexa a la estructura que describe el tipo de medio.

Al enumerar un tipo de salida mediante un objeto de codificador, el miembro **pbFormat** de la estructura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) apuntará a una **estructura DE FORMACUCIÓNATEX.** Esta estructura tiene datos de formato extendido anexados y el tamaño de los datos se almacena en el miembro **DESATEX.cbSize.** Independientemente del contenedor que se use para almacenar los datos comprimidos, debe conservar la estructura **DESATEX** y usarla en el tipo de entrada para el descodificador. Sin los datos de formato extendido, el descodificador no puede descomprimir el contenido.

Para los formatos de vídeo, debe recuperar manualmente los datos de formato extendido y anexarlos a la **estructura VIDEOINFOHEADER.** Para obtener más información, consulte [Uso de datos privados de códec de vídeo.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preguntas más frecuentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 
