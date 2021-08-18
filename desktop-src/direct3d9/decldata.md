---
description: Describe una declaración de vértice.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5686e3344e4642483490c9bd2892cbc92ade290567107b702cc9c56ff351c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803240"
---
# <a name="decldata"></a>DeclData

Describe una declaración de vértice.

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Donde:

-   nElements: número de elementos de declaración de vértice.
-   Elements \[ nElements: \] matriz de elementos de declaración de vértices.
-   nDWords: número de DWORDS.
-   data \[ nDWords: \] matriz de DWORDS que contienen los datos de cada elemento de vértice.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



