---
title: 'RWStructuredBuffer:: Load (int) (función)'
description: 'Lee los datos del búfer. | RWStructuredBuffer:: Load (int) (función)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998049"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="7d316-105">RWStructuredBuffer:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="7d316-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="7d316-106">Lee los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="7d316-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d316-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d316-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="7d316-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d316-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d316-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7d316-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d316-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7d316-110">Type: **int**</span></span>

<span data-ttu-id="7d316-111">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="7d316-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d316-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d316-112">Return value</span></span>

<span data-ttu-id="7d316-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="7d316-113">Type:</span></span>

<span data-ttu-id="7d316-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7d316-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d316-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d316-115">Remarks</span></span>

<span data-ttu-id="7d316-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7d316-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7d316-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="7d316-117">Vertex</span></span> | <span data-ttu-id="7d316-118">Casco</span><span class="sxs-lookup"><span data-stu-id="7d316-118">Hull</span></span> | <span data-ttu-id="7d316-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="7d316-119">Domain</span></span> | <span data-ttu-id="7d316-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="7d316-120">Geometry</span></span> | <span data-ttu-id="7d316-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="7d316-121">Pixel</span></span> | <span data-ttu-id="7d316-122">Compute</span><span class="sxs-lookup"><span data-stu-id="7d316-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7d316-123">x</span><span class="sxs-lookup"><span data-stu-id="7d316-123">x</span></span>      | <span data-ttu-id="7d316-124">x</span><span class="sxs-lookup"><span data-stu-id="7d316-124">x</span></span>    | <span data-ttu-id="7d316-125">x</span><span class="sxs-lookup"><span data-stu-id="7d316-125">x</span></span>      | <span data-ttu-id="7d316-126">x</span><span class="sxs-lookup"><span data-stu-id="7d316-126">x</span></span>        | <span data-ttu-id="7d316-127">x</span><span class="sxs-lookup"><span data-stu-id="7d316-127">x</span></span>     | <span data-ttu-id="7d316-128">x</span><span class="sxs-lookup"><span data-stu-id="7d316-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7d316-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d316-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d316-130">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="7d316-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




