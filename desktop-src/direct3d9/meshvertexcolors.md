---
description: Especifica los colores de vértice para una malla, en lugar de aplicar un material por cara o por malla.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035f8d51ae692b0edd20f7b06b5ab8e756ff73d9cd8265d64700ce5374f9a15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628335"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

Especifica los colores de vértice para una malla, en lugar de aplicar un material por cara o por malla.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Donde:

-   nVertexColors: número de colores. Esto coincide con el número de vértices de la malla.
-   array IndexColor vertexColors \[ nVertexColors: \] matriz de colores indizados. Vea [**IndexedColor.**](indexedcolor.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



