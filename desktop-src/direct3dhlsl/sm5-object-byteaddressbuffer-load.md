---
title: 'ByteAddressBuffer:: Load (int) (función)'
description: 'Obtiene un valor. | ByteAddressBuffer:: Load (int) (función)'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
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
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998060"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="ad66b-105">ByteAddressBuffer:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="ad66b-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="ad66b-106">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="ad66b-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad66b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad66b-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="ad66b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad66b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad66b-109">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ad66b-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad66b-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ad66b-110">Type: **int**</span></span>

<span data-ttu-id="ad66b-111">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="ad66b-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad66b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad66b-112">Return value</span></span>

<span data-ttu-id="ad66b-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ad66b-113">Type: **uint**</span></span>

<span data-ttu-id="ad66b-114">Un valor.</span><span class="sxs-lookup"><span data-stu-id="ad66b-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad66b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad66b-115">Remarks</span></span>

<span data-ttu-id="ad66b-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ad66b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ad66b-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="ad66b-117">Vertex</span></span> | <span data-ttu-id="ad66b-118">Casco</span><span class="sxs-lookup"><span data-stu-id="ad66b-118">Hull</span></span> | <span data-ttu-id="ad66b-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="ad66b-119">Domain</span></span> | <span data-ttu-id="ad66b-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="ad66b-120">Geometry</span></span> | <span data-ttu-id="ad66b-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="ad66b-121">Pixel</span></span> | <span data-ttu-id="ad66b-122">Compute</span><span class="sxs-lookup"><span data-stu-id="ad66b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ad66b-123">x</span><span class="sxs-lookup"><span data-stu-id="ad66b-123">x</span></span>      | <span data-ttu-id="ad66b-124">x</span><span class="sxs-lookup"><span data-stu-id="ad66b-124">x</span></span>    | <span data-ttu-id="ad66b-125">x</span><span class="sxs-lookup"><span data-stu-id="ad66b-125">x</span></span>      | <span data-ttu-id="ad66b-126">x</span><span class="sxs-lookup"><span data-stu-id="ad66b-126">x</span></span>        | <span data-ttu-id="ad66b-127">x</span><span class="sxs-lookup"><span data-stu-id="ad66b-127">x</span></span>     | <span data-ttu-id="ad66b-128">x</span><span class="sxs-lookup"><span data-stu-id="ad66b-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ad66b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad66b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad66b-130">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="ad66b-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="ad66b-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ad66b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




