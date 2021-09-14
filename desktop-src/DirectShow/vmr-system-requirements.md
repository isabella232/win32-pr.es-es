---
description: Requisitos del sistema de VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Requisitos del sistema de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272812"
---
# <a name="vmr-system-requirements"></a>Requisitos del sistema de VMR

VmR usa exclusivamente las funcionalidades de procesamiento de gráficos de la tarjeta de presentación del equipo. VMR no realiza ninguna mezcla o representación de vídeo mediante el procesador host, ya que, para ello, afectaría en gran parte a la velocidad de fotogramas y la calidad del vídeo que se muestra. Al aprovechar las nuevas características que ofrece vmr, especialmente la combinación de varias secuencias de vídeo o imágenes de aplicación, el rendimiento general obtenido depende en gran medida de las funcionalidades de la tarjeta gráfica que se usa en el equipo. Las tarjetas gráficas que se realizan bien con VMR tienen integrada la siguiente compatibilidad con hardware:

-   Compatibilidad con YUV y superficies de textura direct3D "sin potencia de 2".
-   La capacidad de stretchblt de las superficies YUV a DirectDraw RGB.
-   Al menos 16 MB de memoria de vídeo si se van a combinar varias secuencias de vídeo. La cantidad real de memoria necesaria depende del tamaño de la imagen de las secuencias de vídeo y de la resolución del modo de presentación que se está utilizando.
-   Compatibilidad con una superposición RGB o la capacidad de combinar con una superficie de superposición YUV.
-   Lacodización de vídeo acelerado por hardware (compatibilidad con la aceleración de vídeo de DirectX).
-   Velocidades de relleno de píxeles altas.

> [!Note]  
> El VMR requiere que el monitor del sistema se establezca para una profundidad de color de al menos 16 bits. El VMR no se puede poner en estado de ejecución si el monitor está establecido para 256 colores. Además, algunas tarjetas de vídeo no pueden realizar operaciones de Direct3D cuando la pantalla está establecida en 24 bits por píxel.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la representación de mezcla de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



