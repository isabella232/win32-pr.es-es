---
description: Formatos de píxeles de rango dinámico altos
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formatos de píxeles de rango dinámico altos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911941"
---
# <a name="high-dynamic-range-pixel-formats"></a>Formatos de píxeles de rango dinámico altos

Los códecs deben usar formatos de píxeles de Windows Imaging Component (WIC) que conserven todo el intervalo dinámico de los datos del sensor subyacente. GUID \_ WICPixelFormat48bppRGB es un formato típico de 16 bits por canal de punto fijo que se puede usar. También se pueden usar otros formatos de precisión más altos. Para habilitar la compatibilidad total con la canalización de representación acelerada de la unidad de procesamiento de gráficos (GPU) de Windows Presentation Foundation, Microsoft recomienda la compatibilidad con un formato de píxel de punto flotante de 32 bits.

Formatos de píxeles de alto color: con Windows 7, se han agregado dos nuevos formatos de píxel de WIC para admitir los nuevos formatos de presentación de color alto. Estos son: GUID \_ WICPixelFormat32bppRGBA1010102 y GUID \_ WICPixelFormat32bppRGBA1010102XR.

El formato de alto color Float de 16 bits por canal (BPC) es compatible con el \_ formato de píxel WICPixelFormat64bppRGBAHalf de GUID existente.

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

 

 



