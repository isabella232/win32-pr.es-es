---
title: 'StructuredBuffer:: Load (int) (función)'
description: 'Lee los datos del búfer. | StructuredBuffer:: Load (int) (función)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986610"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="28111-105">StructuredBuffer:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="28111-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="28111-106">Lee los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="28111-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="28111-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28111-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="28111-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28111-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28111-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="28111-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28111-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="28111-110">Type: **int**</span></span>

<span data-ttu-id="28111-111">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="28111-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28111-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28111-112">Return value</span></span>

<span data-ttu-id="28111-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="28111-113">Type:</span></span>

<span data-ttu-id="28111-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**StructuredBuffer**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="28111-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="28111-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28111-115">Remarks</span></span>

<span data-ttu-id="28111-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="28111-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="28111-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="28111-117">Vertex</span></span> | <span data-ttu-id="28111-118">Casco</span><span class="sxs-lookup"><span data-stu-id="28111-118">Hull</span></span> | <span data-ttu-id="28111-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="28111-119">Domain</span></span> | <span data-ttu-id="28111-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="28111-120">Geometry</span></span> | <span data-ttu-id="28111-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="28111-121">Pixel</span></span> | <span data-ttu-id="28111-122">Compute</span><span class="sxs-lookup"><span data-stu-id="28111-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="28111-123">x</span><span class="sxs-lookup"><span data-stu-id="28111-123">x</span></span>     | <span data-ttu-id="28111-124">x</span><span class="sxs-lookup"><span data-stu-id="28111-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="28111-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="28111-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28111-126">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="28111-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




