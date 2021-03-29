---
title: RWStructuredBuffer::D función ecrementCounter (Httpserv. h)
description: Disminuye el contador oculto del objeto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter de función HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987061"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="1e33f-104">DecrementCounter función)</span><span class="sxs-lookup"><span data-stu-id="1e33f-104">DecrementCounter function</span></span>

<span data-ttu-id="1e33f-105">Disminuye el contador oculto del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e33f-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e33f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e33f-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="1e33f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e33f-107">Parameters</span></span>

<span data-ttu-id="1e33f-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1e33f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e33f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e33f-109">Return value</span></span>

<span data-ttu-id="1e33f-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1e33f-110">Type: **uint**</span></span>

<span data-ttu-id="1e33f-111">Valor del contador posterior a la disminución.</span><span class="sxs-lookup"><span data-stu-id="1e33f-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e33f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e33f-112">Remarks</span></span>

<span data-ttu-id="1e33f-113">La vista de acceso desordenado enlazada debe tener establecido el [**\_ contador D3D11 buffer \_ UAV \_ Flag \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) durante creationfor para que este método funcione.</span><span class="sxs-lookup"><span data-stu-id="1e33f-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="1e33f-114">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1e33f-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1e33f-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="1e33f-115">Vertex</span></span> | <span data-ttu-id="1e33f-116">Casco</span><span class="sxs-lookup"><span data-stu-id="1e33f-116">Hull</span></span> | <span data-ttu-id="1e33f-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="1e33f-117">Domain</span></span> | <span data-ttu-id="1e33f-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="1e33f-118">Geometry</span></span> | <span data-ttu-id="1e33f-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="1e33f-119">Pixel</span></span> | <span data-ttu-id="1e33f-120">Compute</span><span class="sxs-lookup"><span data-stu-id="1e33f-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1e33f-121">x</span><span class="sxs-lookup"><span data-stu-id="1e33f-121">x</span></span>     | <span data-ttu-id="1e33f-122">x</span><span class="sxs-lookup"><span data-stu-id="1e33f-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="1e33f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e33f-123">Requirements</span></span>



| <span data-ttu-id="1e33f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e33f-124">Requirement</span></span> | <span data-ttu-id="1e33f-125">Value</span><span class="sxs-lookup"><span data-stu-id="1e33f-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e33f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e33f-126">Header</span></span><br/> | <dl> <span data-ttu-id="1e33f-127"><dt>Httpserv. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e33f-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e33f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e33f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e33f-129">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="1e33f-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="1e33f-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1e33f-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

