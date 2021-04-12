---
description: Directrices generales para implementar códecs sin formato
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Directrices generales para implementar códecs sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278180"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Directrices generales para implementar códecs sin formato

En comparación con los tipos de imagen no sin procesar, como JPEG o TIFF, hay dos diferencias importantes en el modo en que se espera que los formatos de imagen sin procesar se comporten en Windows:

-   La mayoría de los formatos de imagen sin procesar se supone que son de "solo lectura" y, probablemente, no admiten la codificación de píxeles en formato sin procesar. Sin embargo, dado que Windows Imaging Component (WIC) requiere un codificador para admitir la reescritura de metadatos, los autores de códecs sin formato deben planear la implementación de al menos una clase de codificador esqueleto.
-   La descodificación de una imagen sin formato de tamaño completo puede tardar mucho tiempo en comparación con otros formatos. Por esta razón, Microsoft recomienda que se tomen ciertos enfoques para minimizar la latencia de descodificación y garantizar la compatibilidad con escenarios como la representación rápida de miniaturas y vistas previas.

    Por ejemplo, todos los autores de códecs sin formato deben implementar la interfaz [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , que proporciona un mecanismo para notificar al descodificador de antemano el tamaño del mapa de bits de destino, lo que permite la descodificación optimizada en un tamaño de imagen de salida más pequeño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Instrucciones de WIC para formatos de imagen RAW de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



