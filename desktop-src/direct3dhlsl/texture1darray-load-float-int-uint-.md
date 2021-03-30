---
title: 'Texture1DArray:: Load (int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture1DArray:: Load (int, int, uint) (función)'
ms.assetid: D5877CED-BE73-4E37-B09D-4096726776EC
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
ms.openlocfilehash: ee367aaf98aa971aa10c6859f117f15df9fcdd83
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986391"
---
# <a name="texture1darrayloadintintuint-function"></a><span data-ttu-id="11200-105">Texture1DArray:: Load (int, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="11200-105">Texture1DArray::Load(int,int,uint) function</span></span>

<span data-ttu-id="11200-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="11200-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="11200-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11200-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="11200-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11200-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11200-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="11200-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11200-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="11200-110">Type: **int**</span></span>

<span data-ttu-id="11200-111">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="11200-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="11200-112">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11200-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11200-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="11200-113">Type: **int**</span></span>

<span data-ttu-id="11200-114">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="11200-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="11200-115">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11200-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11200-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="11200-116">Type: **uint**</span></span>

<span data-ttu-id="11200-117">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="11200-117">The status of the operation.</span></span> <span data-ttu-id="11200-118">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="11200-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="11200-119">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="11200-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="11200-120">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="11200-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11200-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11200-121">Return value</span></span>

<span data-ttu-id="11200-122">Escriba:</span><span class="sxs-lookup"><span data-stu-id="11200-122">Type:</span></span>

<span data-ttu-id="11200-123">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture1DArray**](sm5-object-texture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="11200-123">The return type matches the type in the declaration for the [**Texture1DArray**](sm5-object-texture1darray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="11200-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="11200-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11200-125">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="11200-125">Load methods</span></span>](texture1darray-load.md)
</dt> </dl>

 

 
