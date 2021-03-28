---
title: 'Texture2DMSArray:: Load (int, int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture2DMSArray:: Load (int, int, int, uint) (función)'
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: 0065ee5e420c67876b87c67be1f5e5c8ff10e65b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998041"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a><span data-ttu-id="5e6c6-105">Texture2DMSArray:: Load (int, int, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="5e6c6-105">Texture2DMSArray::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="5e6c6-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5e6c6-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6c6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e6c6-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="5e6c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e6c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e6c6-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5e6c6-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6c6-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5e6c6-110">Type: **int**</span></span>

<span data-ttu-id="5e6c6-111">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="5e6c6-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5e6c6-112">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e6c6-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6c6-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5e6c6-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5e6c6-114">Índice de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e6c6-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="5e6c6-115">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e6c6-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6c6-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5e6c6-116">Type: **int**</span></span>

<span data-ttu-id="5e6c6-117">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="5e6c6-117">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="5e6c6-118">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e6c6-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6c6-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5e6c6-119">Type: **uint**</span></span>

<span data-ttu-id="5e6c6-120">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5e6c6-120">The status of the operation.</span></span> <span data-ttu-id="5e6c6-121">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5e6c6-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5e6c6-122">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5e6c6-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5e6c6-123">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="5e6c6-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e6c6-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e6c6-124">Return value</span></span>

<span data-ttu-id="5e6c6-125">Escriba:</span><span class="sxs-lookup"><span data-stu-id="5e6c6-125">Type:</span></span>

<span data-ttu-id="5e6c6-126">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) .</span><span class="sxs-lookup"><span data-stu-id="5e6c6-126">The return type matches the type in the declaration for the [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e6c6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e6c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6c6-128">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="5e6c6-128">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="5e6c6-129">**Texture2DMSArray**</span><span class="sxs-lookup"><span data-stu-id="5e6c6-129">**Texture2DMSArray**</span></span>](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
