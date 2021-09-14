---
description: Configuración de lacoding de vídeo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configuración de la descodación de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361161"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configuración de la descodación de vídeo (Microsoft Media Foundation)

La codificación es básicamente lo contrario a la codificación en términos de configuración. El descodificador admite muy pocas propiedades y no se requiere ninguna de ellas. Establezca el tipo de entrada en el tipo utilizado para la salida del descodificador (incluidos los datos privados del códec). A continuación, establezca la salida en el formato sin comprimir deseado, establezca la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para reflejar el tamaño de fotograma adecuado e inicie el procesamiento de muestras.

Debe proporcionar al descodificador un tipo de medio que incluya los datos privados del códec situados inmediatamente después de la [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) El descodificador no puede descodificar el contenido sin estos datos. La validación de formato realizada por el descodificador no valida los datos privados. Si faltan los datos privados del códec o son incorrectos, el descodificador responde como si la secuencia de bits esté dañada. Para obtener más información, consulte [Uso de datos privados de códec de vídeo.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de datos privados de códec de vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
