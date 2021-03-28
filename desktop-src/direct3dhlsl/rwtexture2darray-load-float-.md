---
title: 'RWTexture2DArray:: Load (int) (función)'
description: 'Lee los datos de textura. | RWTexture2DArray:: Load (int) (función)'
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
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
ms.openlocfilehash: b23439d471f4d22c807c8d45bb00c23a7d814e3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362197"
---
# <a name="rwtexture2darrayloadint-function"></a><span data-ttu-id="bd91a-105">RWTexture2DArray:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="bd91a-105">RWTexture2DArray::Load(int) function</span></span>

<span data-ttu-id="bd91a-106">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="bd91a-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd91a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd91a-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="bd91a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd91a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd91a-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bd91a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd91a-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bd91a-110">Type: **int**</span></span>

<span data-ttu-id="bd91a-111">Ubicación de la textura.</span><span class="sxs-lookup"><span data-stu-id="bd91a-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd91a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd91a-112">Return value</span></span>

<span data-ttu-id="bd91a-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="bd91a-113">Type:</span></span>

<span data-ttu-id="bd91a-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="bd91a-114">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd91a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd91a-115">Remarks</span></span>

<span data-ttu-id="bd91a-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="bd91a-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bd91a-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="bd91a-117">Vertex</span></span> | <span data-ttu-id="bd91a-118">Casco</span><span class="sxs-lookup"><span data-stu-id="bd91a-118">Hull</span></span> | <span data-ttu-id="bd91a-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="bd91a-119">Domain</span></span> | <span data-ttu-id="bd91a-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="bd91a-120">Geometry</span></span> | <span data-ttu-id="bd91a-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="bd91a-121">Pixel</span></span> | <span data-ttu-id="bd91a-122">Compute</span><span class="sxs-lookup"><span data-stu-id="bd91a-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bd91a-123">x</span><span class="sxs-lookup"><span data-stu-id="bd91a-123">x</span></span>     | <span data-ttu-id="bd91a-124">x</span><span class="sxs-lookup"><span data-stu-id="bd91a-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bd91a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd91a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd91a-126">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="bd91a-126">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 




