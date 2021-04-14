---
title: 'Texture2DMS:: Load (int, int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture2DMS:: Load (int, int, int, uint) (función)'
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362013"
---
# <a name="texture2dmsloadintintintuint-function"></a><span data-ttu-id="79cc7-105">Texture2DMS:: Load (int, int, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="79cc7-105">Texture2DMS::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="79cc7-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="79cc7-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="79cc7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79cc7-107">Syntax</span></span>


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="79cc7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79cc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79cc7-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="79cc7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79cc7-110">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="79cc7-110">Type: **int2**</span></span>

<span data-ttu-id="79cc7-111">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="79cc7-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="79cc7-112">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79cc7-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79cc7-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="79cc7-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="79cc7-114">Índice de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="79cc7-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="79cc7-115">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79cc7-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79cc7-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="79cc7-116">Type: **int2**</span></span>

<span data-ttu-id="79cc7-117">Desplazamiento aplicado a las coordenadas de textura antes de cargar.</span><span class="sxs-lookup"><span data-stu-id="79cc7-117">An offset applied to the texture coordinates before loading.</span></span>

</dd> <dt>

<span data-ttu-id="79cc7-118">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79cc7-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79cc7-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="79cc7-119">Type: **uint**</span></span>

<span data-ttu-id="79cc7-120">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="79cc7-120">The status of the operation.</span></span> <span data-ttu-id="79cc7-121">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="79cc7-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="79cc7-122">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="79cc7-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="79cc7-123">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="79cc7-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79cc7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79cc7-124">Return value</span></span>

<span data-ttu-id="79cc7-125">Escriba:</span><span class="sxs-lookup"><span data-stu-id="79cc7-125">Type:</span></span>

<span data-ttu-id="79cc7-126">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture2DMS**](sm5-object-texture2dms.md) .</span><span class="sxs-lookup"><span data-stu-id="79cc7-126">The return type matches the type in the declaration for the [**Texture2DMS**](sm5-object-texture2dms.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="79cc7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="79cc7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79cc7-128">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="79cc7-128">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="79cc7-129">**Texture2DMS**</span><span class="sxs-lookup"><span data-stu-id="79cc7-129">**Texture2DMS**</span></span>](sm5-object-texture2dms.md)
</dt> </dl>

 

 
