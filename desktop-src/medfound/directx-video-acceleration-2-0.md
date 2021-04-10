---
description: Aceleración de vídeo de DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Aceleración de vídeo de DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275119"
---
# <a name="directx-video-acceleration-20"></a>Aceleración de vídeo de DirectX 2,0

DirectX video Acceleration (DXVA) es una API y una DDI correspondiente para usar la aceleración de hardware para acelerar el procesamiento de códecs de vídeo. Los códecs de software y los procesadores de vídeo de software pueden usar DXVA para descargar ciertas operaciones de uso intensivo de la CPU en la GPU. Por ejemplo, un descodificador de software puede descargar la transformación de coseno discreto inverso (iDCT) en la GPU.

Esta sección contiene los temas siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de DXVA 2,0](about-dxva-2-0.md)<br/>                                                   | Información general de DXVA 2 y su relación con DXVA 1.<br/>                                                                                                                                                        |
| [Administrador de dispositivos de Direct3D](direct3d-device-manager.md)<br/>                                 | El administrador de dispositivos de Microsoft Direct3D habilita dos o más objetos para compartir el mismo dispositivo de Microsoft Direct3D 9.<br/>                                                                                      |
| [Compatibilidad con DXVA 2,0 en DirectShow](supporting-dxva-2-0-in-directshow.md)<br/>             | En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en un filtro de descodificador de DirectShow.<br/>                                                                                             |
| [Compatibilidad con DXVA 2,0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md)<br/> | En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en una transformación de Media Foundation (MFT) con Direct3D 9.<br/>                                                                      |
| [Procesamiento de vídeo de DXVA](dxva-video-processing.md)<br/>                                     | El procesamiento de vídeo de DXVA encapsula las funciones del hardware de gráficos que están dedicadas a procesar imágenes de vídeo sin comprimir. Los servicios de procesamiento de vídeo incluyen desentrelazado y combinación de vídeo.<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | Microsoft DirectX video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware. <br/>                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Especificación de DXVA 1](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
