---
title: 'Texture2DArray:: Load (int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture2DArray:: Load (int, int, uint) (función)'
ms.assetid: 551EA931-6D24-478B-B741-3DD5B1E030E2
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
ms.openlocfilehash: 0a1dd61506eba7ea6e334f2b3e3f89dd6bca5873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998121"
---
# <a name="texture2darrayloadintintuint-function"></a><span data-ttu-id="fc87d-105">Texture2DArray:: Load (int, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="fc87d-105">Texture2DArray::Load(int,int,uint) function</span></span>

<span data-ttu-id="fc87d-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fc87d-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc87d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc87d-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="fc87d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc87d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc87d-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fc87d-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc87d-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fc87d-110">Type: **int**</span></span>

<span data-ttu-id="fc87d-111">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fc87d-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="fc87d-112">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc87d-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc87d-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fc87d-113">Type: **int**</span></span>

<span data-ttu-id="fc87d-114">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fc87d-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fc87d-115">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fc87d-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc87d-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fc87d-116">Type: **uint**</span></span>

<span data-ttu-id="fc87d-117">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fc87d-117">The status of the operation.</span></span> <span data-ttu-id="fc87d-118">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fc87d-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fc87d-119">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fc87d-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fc87d-120">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="fc87d-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc87d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc87d-121">Return value</span></span>

<span data-ttu-id="fc87d-122">Escriba:</span><span class="sxs-lookup"><span data-stu-id="fc87d-122">Type:</span></span>

<span data-ttu-id="fc87d-123">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture2DArray**](sm5-object-texture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="fc87d-123">The return type matches the type in the declaration for the [**Texture2DArray**](sm5-object-texture2darray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc87d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc87d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc87d-125">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="fc87d-125">Load methods</span></span>](texture2darray-load.md)
</dt> </dl>

 

 
