---
title: Abort (función) (Corecrt \_ Terminate. h)
description: Envía un mensaje de error a la cola de información y finaliza la llamada a Draw o Dispatch actual que se está ejecutando.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- Abort de la función HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987265"
---
# <a name="abort-function"></a><span data-ttu-id="51b16-104">abort (función)</span><span class="sxs-lookup"><span data-stu-id="51b16-104">abort function</span></span>

<span data-ttu-id="51b16-105">Envía un mensaje de error a la cola de información y finaliza la llamada a Draw o Dispatch actual que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="51b16-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b16-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51b16-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="51b16-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51b16-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="51b16-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="51b16-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51b16-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51b16-109">Return value</span></span>

<span data-ttu-id="51b16-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="51b16-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51b16-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51b16-111">Remarks</span></span>

<span data-ttu-id="51b16-112">Esta operación no hace nada en los rasterizadores que no lo admiten.</span><span class="sxs-lookup"><span data-stu-id="51b16-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="51b16-113">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="51b16-113">Minimum Shader Model</span></span>

<span data-ttu-id="51b16-114">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="51b16-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="51b16-115">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="51b16-115">Shader Model</span></span>                                                        | <span data-ttu-id="51b16-116">Compatible</span><span class="sxs-lookup"><span data-stu-id="51b16-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="51b16-117">Shader Model 4 (DirectX HLSL) o posterior.</span><span class="sxs-lookup"><span data-stu-id="51b16-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="51b16-118">sí</span><span class="sxs-lookup"><span data-stu-id="51b16-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="51b16-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51b16-119">Requirements</span></span>



| <span data-ttu-id="51b16-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51b16-120">Requirement</span></span> | <span data-ttu-id="51b16-121">Value</span><span class="sxs-lookup"><span data-stu-id="51b16-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51b16-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51b16-122">Header</span></span><br/> | <dl> <span data-ttu-id="51b16-123"><dt>Corecrt \_ Terminate. h</dt></span><span class="sxs-lookup"><span data-stu-id="51b16-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b16-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="51b16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b16-125">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="51b16-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





