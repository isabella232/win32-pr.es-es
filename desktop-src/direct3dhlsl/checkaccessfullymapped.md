---
title: CheckAccessFullyMapped función)
description: Determina si todos los valores de una operación de ejemplo, recopilación o carga han tenido acceso a mosaicos asignados en un recurso en mosaico.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped de función HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793179"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="21cb4-104">CheckAccessFullyMapped función)</span><span class="sxs-lookup"><span data-stu-id="21cb4-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="21cb4-105">Determina si todos los valores de una operación de **ejemplo**, **recopilación** o **carga** han tenido acceso a mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="21cb4-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="21cb4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21cb4-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="21cb4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21cb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cb4-108">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="21cb4-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cb4-109">Tipo: **\_ solo uint**</span><span class="sxs-lookup"><span data-stu-id="21cb4-109">Type: **uint\_only**</span></span>

<span data-ttu-id="21cb4-110">Valor de estado que se devuelve de una operación de **ejemplo**, de **recopilación** o de **carga** .</span><span class="sxs-lookup"><span data-stu-id="21cb4-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="21cb4-111">Dado que no puede tener acceso directamente a este valor de estado, debe pasarlo a **CheckAccessFullyMapped**.</span><span class="sxs-lookup"><span data-stu-id="21cb4-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cb4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21cb4-112">Return value</span></span>

<span data-ttu-id="21cb4-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="21cb4-113">Type: **bool**</span></span>

<span data-ttu-id="21cb4-114">Devuelve un valor **booleano** que indica si todos los valores de una operación de **ejemplo**, **recopilación** o **carga** han tenido acceso a mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="21cb4-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="21cb4-115">Devuelve **true** si todos los valores de la operación han tenido acceso a los mosaicos asignados; de lo contrario, devuelve **false** si se tomó algún valor de un mosaico sin asignar.</span><span class="sxs-lookup"><span data-stu-id="21cb4-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="21cb4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21cb4-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="21cb4-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="21cb4-117">Minimum Shader Model</span></span>

<span data-ttu-id="21cb4-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="21cb4-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="21cb4-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="21cb4-119">Shader Model</span></span>                                                                | <span data-ttu-id="21cb4-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="21cb4-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="21cb4-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cb4-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="21cb4-122">sí</span><span class="sxs-lookup"><span data-stu-id="21cb4-122">yes</span></span>       |



 

<span data-ttu-id="21cb4-123">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="21cb4-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="21cb4-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="21cb4-124">Vertex</span></span> | <span data-ttu-id="21cb4-125">Casco</span><span class="sxs-lookup"><span data-stu-id="21cb4-125">Hull</span></span> | <span data-ttu-id="21cb4-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="21cb4-126">Domain</span></span> | <span data-ttu-id="21cb4-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="21cb4-127">Geometry</span></span> | <span data-ttu-id="21cb4-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="21cb4-128">Pixel</span></span> | <span data-ttu-id="21cb4-129">Compute</span><span class="sxs-lookup"><span data-stu-id="21cb4-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="21cb4-130">x</span><span class="sxs-lookup"><span data-stu-id="21cb4-130">x</span></span>     | <span data-ttu-id="21cb4-131">x</span><span class="sxs-lookup"><span data-stu-id="21cb4-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="21cb4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="21cb4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cb4-133">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="21cb4-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 