---
title: 'Buffer:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Buffer:: Operator (función)'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Función de operador de escritura directa
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424175"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="eeb92-105">Buffer:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="eeb92-105">Buffer::Operator  function</span></span>

<span data-ttu-id="eeb92-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eeb92-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb92-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeb92-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="eeb92-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeb92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb92-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="eeb92-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb92-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="eeb92-110">Type: **uint**</span></span>

<span data-ttu-id="eeb92-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="eeb92-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb92-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeb92-112">Return value</span></span>

<span data-ttu-id="eeb92-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="eeb92-113">Type: **R**</span></span>

<span data-ttu-id="eeb92-114">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eeb92-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeb92-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeb92-115">Remarks</span></span>

<span data-ttu-id="eeb92-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="eeb92-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eeb92-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="eeb92-117">Vertex</span></span> | <span data-ttu-id="eeb92-118">Casco</span><span class="sxs-lookup"><span data-stu-id="eeb92-118">Hull</span></span> | <span data-ttu-id="eeb92-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="eeb92-119">Domain</span></span> | <span data-ttu-id="eeb92-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="eeb92-120">Geometry</span></span> | <span data-ttu-id="eeb92-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="eeb92-121">Pixel</span></span> | <span data-ttu-id="eeb92-122">Compute</span><span class="sxs-lookup"><span data-stu-id="eeb92-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="eeb92-123">x</span><span class="sxs-lookup"><span data-stu-id="eeb92-123">x</span></span>     | <span data-ttu-id="eeb92-124">x</span><span class="sxs-lookup"><span data-stu-id="eeb92-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eeb92-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeb92-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb92-126">Buffer</span><span class="sxs-lookup"><span data-stu-id="eeb92-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="eeb92-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="eeb92-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




