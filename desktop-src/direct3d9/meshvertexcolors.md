---
description: Especifica los colores de los vértices de una malla, en lugar de aplicar un material por caras o por malla.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422825"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

Especifica los colores de los vértices de una malla, en lugar de aplicar un material por caras o por malla.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Donde:

-   nVertexColors: número de colores. Coincide con el número de vértices de la malla.
-   array IndexColor vertexColors \[ nVertexColors \] : matriz de colores indexados. Vea [**IndexedColor**](indexedcolor.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



