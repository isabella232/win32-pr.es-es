---
description: Compatibilidad de VMR con la aceleración de vídeo de DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Compatibilidad de VMR con la aceleración de vídeo de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811509"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Compatibilidad de VMR con la aceleración de vídeo de DirectX

DirectX video Acceleration es una interfaz de programación de aplicaciones (API) y una interfaz de controlador de dispositivo (DDI) correspondiente para la aceleración de hardware del procesamiento de descodificación de vídeo digital, con compatibilidad con la combinación alfa para tales propósitos como soporte de subimágenes de DVD. DirectX VA se documenta en el DDK de Windows. La interfaz [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , que proporciona acceso al modo de usuario a la funcionalidad de DirectX va en un dispositivo de hardware, se documenta en este SDK.

VMR admite [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)y su implementación es idéntica al mezclador de superposición anterior, excepto por una diferencia importante. El mezclador de superposición garantiza que la salida se representa en una superficie de superposición, mientras que la VMR puede enviar la salida para su posterior procesamiento, por ejemplo, una operación 3D, o podría enviar la salida a una superficie fuera de la impresión, que luego se blitted a la superficie primaria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo sobre DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



