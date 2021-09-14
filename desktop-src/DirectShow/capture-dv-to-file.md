---
description: Capturar DV en archivo
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturar DV en archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160231"
---
# <a name="capture-dv-to-file"></a>Capturar DV en archivo

En esta sección se describe cómo capturar vídeo digital (DV) desde una cámara DV o desde una cinta VTR.

1.  Cree una instancia del filtro [del controlador MSDV.](msdv-driver.md) Para obtener más información, consulte [Selección de un dispositivo de captura.](selecting-a-capture-device.md)
2.  Inicialice el generador Graph captura, como se describe en [Acerca de la captura Graph Builder](about-the-capture-graph-builder.md).
3.  Compile el gráfico de captura, en función del tipo de archivo de destino:
    -   [Capturar un archivo DV de tipo 1](capture-a-type-1-dv-file.md)
    -   [Capturar un archivo DV de tipo 2](capture-a-type-2-dv-file.md)
    -   [Capturar DV en RGB sin comprimir](capture-dv-to-uncompressed-rgb.md)
4.  Ejecute el gráfico.

La captura desde una cinta VTR funciona igual que la captura de vídeo en directo desde la cámara, salvo que debe reproducir la cinta, tal como se describe en Control de una [cámara DV.](controlling-a-dv-camcorder.md) Para evitar la pérdida de fotogramas, ejecute primero el gráfico y, a continuación, reprodgue la cinta. Cuando haya terminado de transmitir, detenga primero la cinta y, a continuación, detenga el gráfico.

> [!Note]  
> La cámara debe estar en modo VTR. Consulte [Modo de dispositivo](device-mode.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Archivos AVI DV de tipo 1 frente a tipo 2](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



