---
title: printf (función)
description: Envía un mensaje de sombreador personalizado a la cola de información.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- función printf de HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994766"
---
# <a name="printf-function"></a><span data-ttu-id="91d59-104">printf (función)</span><span class="sxs-lookup"><span data-stu-id="91d59-104">printf function</span></span>

<span data-ttu-id="91d59-105">Envía un mensaje de sombreador personalizado a la cola de información.</span><span class="sxs-lookup"><span data-stu-id="91d59-105">Submits a custom shader message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d59-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91d59-106">Syntax</span></span>

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="91d59-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91d59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d59-108">*format*</span><span class="sxs-lookup"><span data-stu-id="91d59-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="91d59-109">Cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="91d59-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="91d59-110">*argumento...*</span><span class="sxs-lookup"><span data-stu-id="91d59-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="91d59-111">Argumentos opcionales.</span><span class="sxs-lookup"><span data-stu-id="91d59-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d59-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91d59-112">Return value</span></span>

<span data-ttu-id="91d59-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="91d59-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d59-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91d59-114">Remarks</span></span>

<span data-ttu-id="91d59-115">Esta operación no hace nada en los dispositivos que no lo admiten.</span><span class="sxs-lookup"><span data-stu-id="91d59-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="91d59-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="91d59-116">Minimum Shader Model</span></span>

<span data-ttu-id="91d59-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d59-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="91d59-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="91d59-118">Shader Model</span></span>                                                        | <span data-ttu-id="91d59-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="91d59-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="91d59-120">Shader Model 4 (DirectX HLSL) o posterior.</span><span class="sxs-lookup"><span data-stu-id="91d59-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="91d59-121">sí</span><span class="sxs-lookup"><span data-stu-id="91d59-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="91d59-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="91d59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d59-123">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="91d59-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




