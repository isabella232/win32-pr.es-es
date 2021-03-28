---
title: 'Texture3D:: Load (int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture3D:: Load (int, int, uint) (función)'
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
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
ms.openlocfilehash: 19522fe60567e55565265ce0c8b5051c7bf7ccdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998029"
---
# <a name="texture3dloadintintuint-function"></a><span data-ttu-id="3f94a-105">Texture3D:: Load (int, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="3f94a-105">Texture3D::Load(int,int,uint) function</span></span>

<span data-ttu-id="3f94a-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3f94a-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f94a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f94a-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="3f94a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f94a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f94a-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3f94a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f94a-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3f94a-110">Type: **int**</span></span>

<span data-ttu-id="3f94a-111">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3f94a-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="3f94a-112">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f94a-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f94a-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3f94a-113">Type: **int**</span></span>

<span data-ttu-id="3f94a-114">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="3f94a-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3f94a-115">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f94a-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f94a-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f94a-116">Type: **uint**</span></span>

<span data-ttu-id="3f94a-117">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3f94a-117">The status of the operation.</span></span> <span data-ttu-id="3f94a-118">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3f94a-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3f94a-119">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3f94a-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3f94a-120">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="3f94a-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f94a-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f94a-121">Return value</span></span>

<span data-ttu-id="3f94a-122">Escriba:</span><span class="sxs-lookup"><span data-stu-id="3f94a-122">Type:</span></span>

<span data-ttu-id="3f94a-123">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture3D**](sm5-object-texture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="3f94a-123">The return type matches the type in the declaration for the [**Texture3D**](sm5-object-texture3d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f94a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f94a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f94a-125">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="3f94a-125">Load methods</span></span>](texture3d-load.md)
</dt> <dt>

[<span data-ttu-id="3f94a-126">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="3f94a-126">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
