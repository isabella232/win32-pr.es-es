---
description: Codificación de vídeo con compresión temporal
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codificación de vídeo con compresión temporal (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706117"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Codificación de vídeo con compresión temporal (Microsoft Media Foundation)

Para lograr los mayores índices de compresión posibles, los códecs Windows Media Video utilizan la *compresión temporal*. La compresión temporal es una técnica para reducir el tamaño de vídeo comprimido sin codificar cada fotograma como una imagen completa. Los fotogramas que se codifican completamente (como una imagen estática) se denominan *fotogramas clave*. Todos los demás fotogramas del vídeo se representan mediante datos que especifican el cambio desde el último fotograma. Estos fotogramas se denominan *fotogramas Delta*.

La cantidad de compresión que se puede lograr mediante la compresión temporal depende del contenido. Si el vídeo es estático, sin mucho movimiento u otros cambios en la imagen, se pueden crear muchos fotogramas Delta para cada fotograma clave. Los fotogramas más Delta que se usan, menor es el flujo de vídeo codificado. Sin embargo, si el vídeo es dinámico, con gran cantidad de movimiento o cambio de color, la ventaja de usar la compresión temporal es menor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



