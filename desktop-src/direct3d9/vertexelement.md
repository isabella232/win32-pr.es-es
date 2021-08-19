---
description: Describe un elemento de vértice individual en una declaración de vértice.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2ecef6cfa8c522532599acef1b83343c64edd2b5eca93fe461d8bf8419ada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518860"
---
# <a name="vertexelement"></a>VertexElement

Describe un elemento de vértice individual en una declaración de vértice.

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

Donde:

-   Tipo: tipo de datos vertex. Vea [**D3DDECLTYPE.**](./d3ddecltype.md)
-   Método: método de procesamiento de teselador. Vea [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Uso: uso previsto de los datos del vértice. Vea [**D3DDECLUSAGE.**](./d3ddeclusage.md)
-   UsageIndex: modifica los datos de uso. Vea [**D3DDECLUSAGE.**](./d3ddeclusage.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
