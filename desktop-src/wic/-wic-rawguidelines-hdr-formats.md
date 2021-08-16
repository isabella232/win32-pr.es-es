---
description: Alto rango dinámico de píxeles
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Alto rango dinámico de píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086918"
---
# <a name="high-dynamic-range-pixel-formats"></a>Alto rango dinámico de píxeles

Los códecs deben usar Windows de píxeles del componente de creación de imágenes (WIC) que conserven todo el intervalo dinámico de los datos del sensor subyacente. GUID WICPixelFormat48bppRGB es un formato típico de punto fijo de 16 bits por canal que \_ se puede usar. También se pueden usar otros formatos de mayor precisión. Para habilitar la compatibilidad completa con la canalización de representación acelerada de la unidad de procesamiento gráfico (GPU) de Windows Presentation Foundation, Microsoft recomienda encarecidamente la compatibilidad con un formato de píxel de punto flotante de 32 bits.

Formatos de píxeles de color alto: con Windows 7, se han agregado dos nuevos formatos de píxel wic para admitir los nuevos formatos de presentación de color alto. Estos son: GUID \_ WICPixelFormat32bppRGBA1010102 y GUID \_ WICPixelFormat32bppRGBA1010102XR.

El formato de color alto flotante de 16 bits por canal (bpc) es compatible con el formato de píxel \_ WICPixelFormat64bppRGBAHalf existente.

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

 

 



