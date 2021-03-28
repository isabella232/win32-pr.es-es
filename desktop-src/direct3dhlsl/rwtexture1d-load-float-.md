---
title: 'RWTexture1D:: Load (int) (función)'
description: 'Lee los datos de textura. | RWTexture1D:: Load (int) (función)'
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362222"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="3f641-105">RWTexture1D:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="3f641-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="3f641-106">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="3f641-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f641-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f641-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="3f641-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f641-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3f641-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f641-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3f641-110">Type: **int**</span></span>

<span data-ttu-id="3f641-111">Ubicación de la textura.</span><span class="sxs-lookup"><span data-stu-id="3f641-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f641-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f641-112">Return value</span></span>

<span data-ttu-id="3f641-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="3f641-113">Type:</span></span>

<span data-ttu-id="3f641-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="3f641-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f641-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f641-115">Remarks</span></span>

<span data-ttu-id="3f641-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3f641-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3f641-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="3f641-117">Vertex</span></span> | <span data-ttu-id="3f641-118">Casco</span><span class="sxs-lookup"><span data-stu-id="3f641-118">Hull</span></span> | <span data-ttu-id="3f641-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="3f641-119">Domain</span></span> | <span data-ttu-id="3f641-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="3f641-120">Geometry</span></span> | <span data-ttu-id="3f641-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="3f641-121">Pixel</span></span> | <span data-ttu-id="3f641-122">Compute</span><span class="sxs-lookup"><span data-stu-id="3f641-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3f641-123">x</span><span class="sxs-lookup"><span data-stu-id="3f641-123">x</span></span>     | <span data-ttu-id="3f641-124">x</span><span class="sxs-lookup"><span data-stu-id="3f641-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3f641-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f641-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f641-126">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="3f641-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




