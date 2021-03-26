---
title: 'RWBuffer:: Load (int) (función)'
description: 'Lee los datos del búfer. | RWBuffer:: Load (int) (función)'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820610"
---
# <a name="rwbufferloadint-function"></a><span data-ttu-id="8206c-105">RWBuffer:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="8206c-105">RWBuffer::Load(int) function</span></span>

<span data-ttu-id="8206c-106">Lee los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="8206c-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8206c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8206c-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="8206c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8206c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8206c-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8206c-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8206c-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="8206c-110">Type: **int**</span></span>

<span data-ttu-id="8206c-111">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="8206c-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8206c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8206c-112">Return value</span></span>

<span data-ttu-id="8206c-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="8206c-113">Type:</span></span>

<span data-ttu-id="8206c-114">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8206c-114">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8206c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8206c-115">Remarks</span></span>

<span data-ttu-id="8206c-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8206c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8206c-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="8206c-117">Vertex</span></span> | <span data-ttu-id="8206c-118">Casco</span><span class="sxs-lookup"><span data-stu-id="8206c-118">Hull</span></span> | <span data-ttu-id="8206c-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="8206c-119">Domain</span></span> | <span data-ttu-id="8206c-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="8206c-120">Geometry</span></span> | <span data-ttu-id="8206c-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="8206c-121">Pixel</span></span> | <span data-ttu-id="8206c-122">Compute</span><span class="sxs-lookup"><span data-stu-id="8206c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8206c-123">x</span><span class="sxs-lookup"><span data-stu-id="8206c-123">x</span></span>      | <span data-ttu-id="8206c-124">x</span><span class="sxs-lookup"><span data-stu-id="8206c-124">x</span></span>    | <span data-ttu-id="8206c-125">x</span><span class="sxs-lookup"><span data-stu-id="8206c-125">x</span></span>      | <span data-ttu-id="8206c-126">x</span><span class="sxs-lookup"><span data-stu-id="8206c-126">x</span></span>        | <span data-ttu-id="8206c-127">x</span><span class="sxs-lookup"><span data-stu-id="8206c-127">x</span></span>     | <span data-ttu-id="8206c-128">x</span><span class="sxs-lookup"><span data-stu-id="8206c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8206c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8206c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8206c-130">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="8206c-130">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 




