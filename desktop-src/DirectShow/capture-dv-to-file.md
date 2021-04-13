---
description: Capturar DV en archivo
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturar DV en archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359982"
---
# <a name="capture-dv-to-file"></a>Capturar DV en archivo

En esta sección se describe cómo capturar vídeo digital (DV) desde una cámara DV o desde una cinta VTR.

1.  Cree una instancia del filtro del [controlador MSDV](msdv-driver.md) . Para obtener más información, consulte [seleccionar un dispositivo de captura](selecting-a-capture-device.md).
2.  Inicialice el generador de gráficos de captura, tal y como se describe en [el generador de gráficos de captura](about-the-capture-graph-builder.md).
3.  Cree el gráfico de captura, en función del tipo de archivo de destino:
    -   [Capturar un archivo de tipo 1 DV](capture-a-type-1-dv-file.md)
    -   [Capturar un archivo de tipo-2 DV](capture-a-type-2-dv-file.md)
    -   [Capturar DV en RGB sin comprimir](capture-dv-to-uncompressed-rgb.md)
4.  Ejecute el gráfico.

La captura de una cinta VTR funciona igual que la captura de vídeo en directo desde la cámara, salvo que se debe reproducir la cinta, tal como se describe en [controlar una videocámara DV](controlling-a-dv-camcorder.md). Para evitar la pérdida de fotogramas, ejecute primero el gráfico y, a continuación, reproduzca la cinta. Cuando haya terminado de transmitir, detenga primero la cinta y, a continuación, detenga el gráfico.

> [!Note]  
> El camascopio debe estar en modo VTR. Vea [modo de dispositivo](device-mode.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Archivos AVI de tipo 1 frente a-2](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



