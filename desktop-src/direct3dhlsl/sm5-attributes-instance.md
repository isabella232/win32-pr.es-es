---
title: instance
description: Use este atributo para instanciar un sombreador de geometría.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077113"
---
# <a name="instance"></a><span data-ttu-id="0b8b4-103">instance</span><span class="sxs-lookup"><span data-stu-id="0b8b4-103">instance</span></span>

<span data-ttu-id="0b8b4-104">Use este atributo para instanciar un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0b8b4-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="0b8b4-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b8b4-105">Remarks</span></span>

<span data-ttu-id="0b8b4-106">X es un índice entero que indica el número de instancias que se van a ejecutar para cada elemento dibujado (por ejemplo, para cada triángulo).</span><span class="sxs-lookup"><span data-stu-id="0b8b4-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="0b8b4-107">Al utilizar este atributo, use [VP \_ GSInstanceID](sv-gsinstanceid.md) para identificar qué instancia de un sombreador de geometría se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0b8b4-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="0b8b4-108">Este atributo es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0b8b4-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="0b8b4-109">Vértice</span><span class="sxs-lookup"><span data-stu-id="0b8b4-109">Vertex</span></span> | <span data-ttu-id="0b8b4-110">Casco</span><span class="sxs-lookup"><span data-stu-id="0b8b4-110">Hull</span></span> | <span data-ttu-id="0b8b4-111">Dominio</span><span class="sxs-lookup"><span data-stu-id="0b8b4-111">Domain</span></span> | <span data-ttu-id="0b8b4-112">Geometría</span><span class="sxs-lookup"><span data-stu-id="0b8b4-112">Geometry</span></span> | <span data-ttu-id="0b8b4-113">Píxel</span><span class="sxs-lookup"><span data-stu-id="0b8b4-113">Pixel</span></span> | <span data-ttu-id="0b8b4-114">Compute</span><span class="sxs-lookup"><span data-stu-id="0b8b4-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="0b8b4-115">x</span><span class="sxs-lookup"><span data-stu-id="0b8b4-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="0b8b4-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b8b4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b8b4-117">Atributos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0b8b4-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b8b4-118">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0b8b4-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




