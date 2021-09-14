---
description: Directrices generales para implementar códecs RAW
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Directrices generales para implementar códecs RAW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256455"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Directrices generales para implementar códecs RAW

En comparación con los tipos de imágenes que no son RAW, como JPEG o TIFF, hay dos diferencias importantes en la forma en que se espera que los formatos de imagen RAW se comporten en Windows:

-   Se supone que la mayoría de los formatos de imagen RAW son de "solo lectura" y probablemente no admitirán la codificación de píxeles en formato RAW. Sin embargo, dado Windows Imaging Component (WIC) requiere un codificador para admitir la reescribición de metadatos, los autores de códecs RAW deben planear implementar al menos una clase de codificador de esqueleto.
-   La decodificación de una imagen RAW de tamaño completo puede tardar mucho tiempo en comparación con otros formatos. Por este motivo, Microsoft recomienda adoptar determinados enfoques para minimizar la latencia de lacoding y para garantizar la compatibilidad con escenarios como la representación rápida de miniaturas y vistas previas.

    Por ejemplo, todos los autores de códecs RAW deben implementar la interfaz [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) que proporciona un mecanismo para notificar al descodificador antes del tamaño del mapa de bits de destino, lo que permite descodificar optimizado a un tamaño de imagen de salida más pequeño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen raw de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



