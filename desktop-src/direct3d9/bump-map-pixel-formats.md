---
description: Un mapa de rugosidad es un objeto IDirect3DTexture9 que usa un formato de píxel especializado.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formatos de píxeles de mapa de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080261"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formatos de píxeles de mapa de rugosidad (Direct3D 9)

Un mapa de rugosidad es un objeto [**IDirect3DTexture9**](/windows/desktop/api) que usa un formato de píxel especializado. En lugar de almacenar los componentes de color rojo, verde y azul, cada píxel de un mapa de rugosidad almacena los valores Delta para usted y v (D<sub>U</sub> y d<sub>v</sub>) y, en ocasiones, un componente de luminancia, L. Estos valores son aplicados por el sistema tal y como se describe en el tema [fórmulas de asignación de rugosidad (Direct3D 9)](bump-mapping-formulas.md) .

Puede especificar un formato de píxel de mapa de rugosidad estableciendo el formato en uno de los siguientes: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 o D3DFMT \_ V16U16. Para obtener descripciones, vea [D3DFORMAT](d3dformat.md).

Los componentes D<sub>U</sub> y d<sub>V</sub> de un píxel son valores con signo comprendidos entre-1,0 y + 1,0. El componente de luminancia, cuando se utiliza, es un valor entero sin signo que va de 0 a 255.

> [!Note]  
> Antes de seleccionar un formato de píxel de mapa de rugosidad, compruebe si se admite el formato determinado. Para obtener más información, vea [usar la asignación de rugosidad (Direct3D 9)](using-bump-mapping.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de rugosidad](bump-mapping.md)
</dt> </dl>

 

 



