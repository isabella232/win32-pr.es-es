---
description: VMR requisitos del sistema
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR requisitos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277581"
---
# <a name="vmr-system-requirements"></a>VMR requisitos del sistema

La VMR utiliza exclusivamente las capacidades de procesamiento de gráficos de la tarjeta de presentación del equipo; la VMR no realiza ninguna fusión ni representación de vídeo con el procesador del host, porque para ello afectaría en gran medida a la velocidad de fotogramas y la calidad del vídeo que se muestra. Cuando se aprovechan las nuevas características que ofrece la VMR, especialmente la combinación de varias secuencias de vídeo o imágenes de aplicaciones, el rendimiento general obtenido depende en gran medida de las capacidades de la tarjeta gráfica que se usa en el equipo. Las tarjetas gráficas que funcionan bien con la VMR tienen la siguiente compatibilidad de hardware integrada:

-   Compatibilidad con las superficies de textura de Direct3D de YUV y "no potencia de 2".
-   La capacidad de StretchBlt de las superficies YUV a RGB DirectDraw.
-   Al menos 16 MB de memoria de vídeo si se van a combinar varias secuencias de vídeo. La cantidad real de memoria necesaria depende del tamaño de la imagen de las secuencias de vídeo y la resolución del modo de presentación que se está usando.
-   Compatibilidad con una superposición de RGB o la capacidad de fusionar con una superficie de superposición de YUV.
-   Vídeo acelerado por hardware (compatibilidad con la aceleración de vídeo de DirectX).
-   Tasas de relleno de alto nivel de píxeles.

> [!Note]  
> La VMR requiere que el monitor de sistema se establezca para una profundidad de color de al menos 16 bits. No se puede poner VMR en un estado de ejecución si el monitor está configurado para 256 colores. Además, algunas tarjetas de vídeo no pueden realizar operaciones de Direct3D cuando la pantalla se establece en 24 bits por píxel.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la presentación de la combinación de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



