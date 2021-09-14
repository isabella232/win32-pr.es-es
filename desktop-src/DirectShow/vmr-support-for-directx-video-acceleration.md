---
description: Compatibilidad de VMR con la aceleración de vídeo de DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Compatibilidad de VMR con la aceleración de vídeo de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272820"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Compatibilidad de VMR con la aceleración de vídeo de DirectX

La aceleración de vídeo de DirectX es una interfaz de programación de aplicaciones (API) y una interfaz de controlador de dispositivo (DDI) correspondiente para la aceleración de hardware del procesamiento de lacodización de vídeo digital, con compatibilidad con la mezcla alfa para fines como la compatibilidad con subpicture de DVD. DirectX VA se documenta en el Windows DDK. La [**interfaz IAMVideoAccelerator,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) que proporciona acceso en modo de usuario a la funcionalidad de DirectX VA en un dispositivo de hardware, se documenta en este SDK.

VmR admite [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)y su implementación es idéntica a la versión anterior Mixer excepto por una diferencia importante. El Mixer superposición garantiza que la salida se representa en una superficie superpuesta, mientras que el VMR puede enviar la salida para su posterior procesamiento, por ejemplo, una operación 3D, o bien podría enviar la salida a una superficie fuera de pantalla que, a continuación, se divide en la superficie principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la aceleración de vídeo de DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



