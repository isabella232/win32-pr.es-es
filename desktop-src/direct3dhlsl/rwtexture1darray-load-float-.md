---
title: 'RWTexture1DArray:: Load (int) (función)'
description: 'Lee los datos de textura. | RWTexture1DArray:: Load (int) (función)'
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986282"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="6466d-105">RWTexture1DArray:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="6466d-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="6466d-106">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="6466d-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6466d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6466d-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="6466d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6466d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6466d-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6466d-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6466d-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6466d-110">Type: **int**</span></span>

<span data-ttu-id="6466d-111">Ubicación de la textura.</span><span class="sxs-lookup"><span data-stu-id="6466d-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6466d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6466d-112">Return value</span></span>

<span data-ttu-id="6466d-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="6466d-113">Type:</span></span>

<span data-ttu-id="6466d-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="6466d-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6466d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6466d-115">Remarks</span></span>

<span data-ttu-id="6466d-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6466d-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6466d-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="6466d-117">Vertex</span></span> | <span data-ttu-id="6466d-118">Casco</span><span class="sxs-lookup"><span data-stu-id="6466d-118">Hull</span></span> | <span data-ttu-id="6466d-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="6466d-119">Domain</span></span> | <span data-ttu-id="6466d-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="6466d-120">Geometry</span></span> | <span data-ttu-id="6466d-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="6466d-121">Pixel</span></span> | <span data-ttu-id="6466d-122">Compute</span><span class="sxs-lookup"><span data-stu-id="6466d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6466d-123">x</span><span class="sxs-lookup"><span data-stu-id="6466d-123">x</span></span>     | <span data-ttu-id="6466d-124">x</span><span class="sxs-lookup"><span data-stu-id="6466d-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6466d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6466d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6466d-126">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="6466d-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




