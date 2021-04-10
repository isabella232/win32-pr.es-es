---
description: Describe un elemento de vértice individual en una declaración de vértice.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152410"
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

-   Tipo de datos de tipo de vértice. Vea [**D3DDECLTYPE**](./d3ddecltype.md).
-   Método: método de procesamiento del teselador. Vea [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Uso previsto de los datos de vértices. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   UsageIndex: modifica los datos de uso. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
