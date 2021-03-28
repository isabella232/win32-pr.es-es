---
title: maxtessfactor
description: Indica el valor máximo que el sombreador de casco devolverá para cualquier factor de teselación.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904297"
---
# <a name="maxtessfactor"></a><span data-ttu-id="2dbb2-103">maxtessfactor</span><span class="sxs-lookup"><span data-stu-id="2dbb2-103">maxtessfactor</span></span>

<span data-ttu-id="2dbb2-104">Indica el valor máximo que el sombreador de casco devolverá para cualquier factor de teselación.</span><span class="sxs-lookup"><span data-stu-id="2dbb2-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="2dbb2-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dbb2-105">Remarks</span></span>

<span data-ttu-id="2dbb2-106">Este atributo coloca un límite superior en la cantidad de teselación solicitada para ayudar a un controlador a determinar la cantidad máxima de recursos necesarios para la teselación.</span><span class="sxs-lookup"><span data-stu-id="2dbb2-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="2dbb2-107">Este atributo es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2dbb2-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2dbb2-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="2dbb2-108">Vertex</span></span> | <span data-ttu-id="2dbb2-109">Casco</span><span class="sxs-lookup"><span data-stu-id="2dbb2-109">Hull</span></span> | <span data-ttu-id="2dbb2-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="2dbb2-110">Domain</span></span> | <span data-ttu-id="2dbb2-111">Geometría</span><span class="sxs-lookup"><span data-stu-id="2dbb2-111">Geometry</span></span> | <span data-ttu-id="2dbb2-112">Píxel</span><span class="sxs-lookup"><span data-stu-id="2dbb2-112">Pixel</span></span> | <span data-ttu-id="2dbb2-113">Compute</span><span class="sxs-lookup"><span data-stu-id="2dbb2-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="2dbb2-114">x</span><span class="sxs-lookup"><span data-stu-id="2dbb2-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="2dbb2-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2dbb2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dbb2-116">Atributos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2dbb2-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="2dbb2-117">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2dbb2-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




