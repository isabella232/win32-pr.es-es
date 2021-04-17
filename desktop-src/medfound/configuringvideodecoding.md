---
description: Configuración de la descodificación de vídeo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configuración de la descodificación de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705420"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configuración de la descodificación de vídeo (Microsoft Media Foundation)

La descodificación es esencialmente la opuesta a la codificación en cuanto a la configuración. El descodificador admite muy pocas propiedades y no se requiere ninguna. Establezca el tipo de entrada en el tipo que se usa para la salida del descodificador (incluidos los datos privados del códec). A continuación, establezca la salida en el formato sin comprimir deseado, establezca la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para que refleje el tamaño de fotograma adecuado y comience a procesar ejemplos.

Debe proporcionar el descodificador con un tipo de medio que incluya los datos privados del códec situados inmediatamente después de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . El descodificador no puede descodificar el contenido sin estos datos. La validación de formato realizada por el descodificador no valida los datos privados. Si los datos privados del códec faltan o son incorrectos, el descodificador responde como si el flujo de bits estuviera dañado. Para obtener más información, consulte [uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
