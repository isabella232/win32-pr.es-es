---
title: 'RWTexture3D:: Load (int) (función)'
description: 'Lee los datos de textura. | RWTexture3D:: Load (int) (función)'
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362219"
---
# <a name="rwtexture3dloadint-function"></a><span data-ttu-id="26149-105">RWTexture3D:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="26149-105">RWTexture3D::Load(int) function</span></span>

<span data-ttu-id="26149-106">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="26149-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="26149-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26149-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="26149-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26149-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26149-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="26149-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26149-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="26149-110">Type: **int**</span></span>

<span data-ttu-id="26149-111">Ubicación de la textura.</span><span class="sxs-lookup"><span data-stu-id="26149-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26149-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26149-112">Return value</span></span>

<span data-ttu-id="26149-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="26149-113">Type:</span></span>

<span data-ttu-id="26149-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture3D**](sm5-object-rwtexture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="26149-114">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26149-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26149-115">Remarks</span></span>

<span data-ttu-id="26149-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="26149-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="26149-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="26149-117">Vertex</span></span> | <span data-ttu-id="26149-118">Casco</span><span class="sxs-lookup"><span data-stu-id="26149-118">Hull</span></span> | <span data-ttu-id="26149-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="26149-119">Domain</span></span> | <span data-ttu-id="26149-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="26149-120">Geometry</span></span> | <span data-ttu-id="26149-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="26149-121">Pixel</span></span> | <span data-ttu-id="26149-122">Compute</span><span class="sxs-lookup"><span data-stu-id="26149-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="26149-123">x</span><span class="sxs-lookup"><span data-stu-id="26149-123">x</span></span>     | <span data-ttu-id="26149-124">x</span><span class="sxs-lookup"><span data-stu-id="26149-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="26149-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="26149-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26149-126">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="26149-126">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 




