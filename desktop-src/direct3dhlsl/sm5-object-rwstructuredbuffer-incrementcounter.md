---
title: 'RWStructuredBuffer:: IncrementCounter (función) (Httpserv. h)'
description: Incrementa el contador oculto del objeto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter de función HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362698"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="8b66c-104">IncrementCounter función)</span><span class="sxs-lookup"><span data-stu-id="8b66c-104">IncrementCounter function</span></span>

<span data-ttu-id="8b66c-105">Incrementa el contador oculto del objeto.</span><span class="sxs-lookup"><span data-stu-id="8b66c-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b66c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b66c-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="8b66c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b66c-107">Parameters</span></span>

<span data-ttu-id="8b66c-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8b66c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b66c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b66c-109">Return value</span></span>

<span data-ttu-id="8b66c-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8b66c-110">Type: **uint**</span></span>

<span data-ttu-id="8b66c-111">Valor del contador previamente incrementado.</span><span class="sxs-lookup"><span data-stu-id="8b66c-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b66c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b66c-112">Remarks</span></span>

<span data-ttu-id="8b66c-113">La vista de acceso desordenado enlazada debe tener establecido el [**contador D3D11 de \_ búfer \_ UAV \_ \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) en el conjunto de búferes de la creación para que este método funcione.</span><span class="sxs-lookup"><span data-stu-id="8b66c-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="8b66c-114">Un recurso estructurado se puede indexar más en función de los nombres de componente de las estructuras.</span><span class="sxs-lookup"><span data-stu-id="8b66c-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="8b66c-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8b66c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8b66c-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="8b66c-116">Vertex</span></span> | <span data-ttu-id="8b66c-117">Casco</span><span class="sxs-lookup"><span data-stu-id="8b66c-117">Hull</span></span> | <span data-ttu-id="8b66c-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="8b66c-118">Domain</span></span> | <span data-ttu-id="8b66c-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="8b66c-119">Geometry</span></span> | <span data-ttu-id="8b66c-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="8b66c-120">Pixel</span></span> | <span data-ttu-id="8b66c-121">Compute</span><span class="sxs-lookup"><span data-stu-id="8b66c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8b66c-122">x</span><span class="sxs-lookup"><span data-stu-id="8b66c-122">x</span></span>     | <span data-ttu-id="8b66c-123">x</span><span class="sxs-lookup"><span data-stu-id="8b66c-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="8b66c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b66c-124">Requirements</span></span>



| <span data-ttu-id="8b66c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b66c-125">Requirement</span></span> | <span data-ttu-id="8b66c-126">Value</span><span class="sxs-lookup"><span data-stu-id="8b66c-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b66c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b66c-127">Header</span></span><br/> | <dl> <span data-ttu-id="8b66c-128"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b66c-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b66c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b66c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b66c-130">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="8b66c-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="8b66c-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8b66c-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

