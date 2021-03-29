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
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="9f9f2-103">Compatibilidad de VMR con la aceleración de vídeo de DirectX</span><span class="sxs-lookup"><span data-stu-id="9f9f2-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="9f9f2-104">DirectX video Acceleration es una interfaz de programación de aplicaciones (API) y una interfaz de controlador de dispositivo (DDI) correspondiente para la aceleración de hardware del procesamiento de descodificación de vídeo digital, con compatibilidad con la combinación alfa para tales propósitos como soporte de subimágenes de DVD.</span><span class="sxs-lookup"><span data-stu-id="9f9f2-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="9f9f2-105">DirectX VA se documenta en el DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f9f2-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="9f9f2-106">La interfaz [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , que proporciona acceso al modo de usuario a la funcionalidad de DirectX va en un dispositivo de hardware, se documenta en este SDK.</span><span class="sxs-lookup"><span data-stu-id="9f9f2-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="9f9f2-107">VMR admite [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)y su implementación es idéntica al mezclador de superposición anterior, excepto por una diferencia importante.</span><span class="sxs-lookup"><span data-stu-id="9f9f2-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="9f9f2-108">El mezclador de superposición garantiza que la salida se representa en una superficie de superposición, mientras que la VMR puede enviar la salida para su posterior procesamiento, por ejemplo, una operación 3D, o podría enviar la salida a una superficie fuera de la impresión, que luego se blitted a la superficie primaria.</span><span class="sxs-lookup"><span data-stu-id="9f9f2-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f9f2-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f9f2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f9f2-110">Aceleración de vídeo sobre DirectX</span><span class="sxs-lookup"><span data-stu-id="9f9f2-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



