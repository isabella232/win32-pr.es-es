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
# <a name="vertexelement"></a><span data-ttu-id="6f96c-103">VertexElement</span><span class="sxs-lookup"><span data-stu-id="6f96c-103">VertexElement</span></span>

<span data-ttu-id="6f96c-104">Describe un elemento de vértice individual en una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="6f96c-104">Describes an individual vertex element in a vertex declaration.</span></span>

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

<span data-ttu-id="6f96c-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="6f96c-105">Where:</span></span>

-   <span data-ttu-id="6f96c-106">Tipo de datos de tipo de vértice.</span><span class="sxs-lookup"><span data-stu-id="6f96c-106">Type - Vertex data type.</span></span> <span data-ttu-id="6f96c-107">Vea [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="6f96c-107">See [**D3DDECLTYPE**](./d3ddecltype.md).</span></span>
-   <span data-ttu-id="6f96c-108">Método: método de procesamiento del teselador.</span><span class="sxs-lookup"><span data-stu-id="6f96c-108">Method - Tessellator processing method.</span></span> <span data-ttu-id="6f96c-109">Vea [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="6f96c-109">See [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>
-   <span data-ttu-id="6f96c-110">Uso previsto de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="6f96c-110">Usage - Intended use of the vertex data.</span></span> <span data-ttu-id="6f96c-111">Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="6f96c-111">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>
-   <span data-ttu-id="6f96c-112">UsageIndex: modifica los datos de uso.</span><span class="sxs-lookup"><span data-stu-id="6f96c-112">UsageIndex - Modifies the usage data.</span></span> <span data-ttu-id="6f96c-113">Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="6f96c-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6f96c-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f96c-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f96c-115">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="6f96c-115">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> <dt>

[<span data-ttu-id="6f96c-116">**D3DVERTEXELEMENT9**</span><span class="sxs-lookup"><span data-stu-id="6f96c-116">**D3DVERTEXELEMENT9**</span></span>](d3dvertexelement9.md)
</dt> </dl>

 

 
