---
description: Un mapa de protuberancias es un objeto IDirect3DTexture9 que usa un formato de píxel especializado.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formatos de píxeles de mapa de protuberancia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f627ce95151207c25e2365d2e467fb94b93cfb5c1bf54ce0c3df401891fcafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805730"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formatos de píxeles de mapa de protuberancia (Direct3D 9)

Un mapa de protuberancias [**es un objeto IDirect3DTexture9**](/windows/desktop/api) que usa un formato de píxel especializado. En lugar de almacenar componentes de color rojo, verde y azul, cada píxel de un mapa de incrementos almacena los valores delta para usted y v (D<sub>U</sub> y D<sub>V)</sub>y, a veces, un componente de luminosidad, L. El sistema aplica estos valores, como se describe en el tema Fórmulas de asignación de cambios [(Direct3D 9).](bump-mapping-formulas.md)

Puede especificar un formato de píxeles de mapa de protuberancia estableciendo el formato en uno de los siguientes: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 o D3DFMT \_ V16U16. Para obtener descripciones, [vea D3DFORMAT.](d3dformat.md)

Los componentes<sub>D U</sub> y D<sub>V</sub> de un píxel son valores con signo que van de - 1.0 a +1.0. El componente de luminosidad, cuando se usa, es un valor entero sin signo que oscila entre 0 y 255.

> [!Note]  
> Antes de seleccionar un formato de píxeles de mapa de protuberancias, compruebe si se admite el formato determinado. Para obtener más información, [vea Usar la asignación de protuberancias (Direct3D 9).](using-bump-mapping.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de protuberancias](bump-mapping.md)
</dt> </dl>

 

 



