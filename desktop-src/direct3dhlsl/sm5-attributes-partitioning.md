---
title: creación de particiones
description: Define el esquema tesselation que se va a usar en el sombreador de casco.
ms.assetid: 29dc4abb-4d29-4538-8680-a4fcbfd8235b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bf0744481a123998b64693d669e9cb7255599f8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904296"
---
# <a name="partitioning"></a><span data-ttu-id="29cb2-103">creación de particiones</span><span class="sxs-lookup"><span data-stu-id="29cb2-103">partitioning</span></span>

<span data-ttu-id="29cb2-104">Define el esquema tesselation que se va a usar en el sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="29cb2-104">Defines the tesselation scheme to be used in the hull shader.</span></span>


```
partitioning(X)    
```



## <a name="remarks"></a><span data-ttu-id="29cb2-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29cb2-105">Remarks</span></span>

<span data-ttu-id="29cb2-106">Puede ser un **entero**, un valor **fraccionario \_ par**, una **fracción \_ impar** o **pow2**.</span><span class="sxs-lookup"><span data-stu-id="29cb2-106">Can be **integer**, **fractional\_even**, **fractional\_odd**, or **pow2**.</span></span>

<span data-ttu-id="29cb2-107">Este atributo es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="29cb2-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="29cb2-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="29cb2-108">Vertex</span></span> | <span data-ttu-id="29cb2-109">Casco</span><span class="sxs-lookup"><span data-stu-id="29cb2-109">Hull</span></span> | <span data-ttu-id="29cb2-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="29cb2-110">Domain</span></span> | <span data-ttu-id="29cb2-111">Geometría</span><span class="sxs-lookup"><span data-stu-id="29cb2-111">Geometry</span></span> | <span data-ttu-id="29cb2-112">Píxel</span><span class="sxs-lookup"><span data-stu-id="29cb2-112">Pixel</span></span> | <span data-ttu-id="29cb2-113">Compute</span><span class="sxs-lookup"><span data-stu-id="29cb2-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="29cb2-114">x</span><span class="sxs-lookup"><span data-stu-id="29cb2-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="29cb2-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29cb2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29cb2-116">Atributos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="29cb2-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="29cb2-117">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="29cb2-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




