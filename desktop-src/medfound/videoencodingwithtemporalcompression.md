---
description: Codificación de vídeo con compresión temporal
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codificación de vídeo con compresión temporal (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467205"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Codificación de vídeo con compresión temporal (Microsoft Media Foundation)

Para lograr las mayores proporciones de compresión posibles, los códecs Windows Media Video usan la *compresión temporal*. La compresión temporal es una técnica para reducir el tamaño de vídeo comprimido al no codificar cada fotograma como una imagen completa. Los fotogramas que se codifican completamente (como una imagen estática) se denominan *fotogramas clave.* Todos los demás fotogramas del vídeo se representan mediante datos que especifican el cambio desde el último fotograma. Estos fotogramas se denominan *marcos delta.*

La cantidad de compresión que se puede lograr mediante la compresión temporal depende del contenido. Si el vídeo es estático, sin mucho movimiento u otros cambios en la imagen, se pueden crear muchos fotogramas delta para cada fotograma clave. Cuanto más fotogramas delta se usan, menor es la secuencia de vídeo codificada. Sin embargo, si el vídeo es dinámico, con mucho movimiento o colores cambiantes, la ventaja de usar la compresión temporal es menor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



