---
title: errorf función)
description: Envía un mensaje de error a la cola de información.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf de función HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076610"
---
# <a name="errorf-function"></a><span data-ttu-id="71d46-104">errorf función)</span><span class="sxs-lookup"><span data-stu-id="71d46-104">errorf function</span></span>

<span data-ttu-id="71d46-105">Envía un mensaje de error a la cola de información.</span><span class="sxs-lookup"><span data-stu-id="71d46-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d46-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71d46-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="71d46-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71d46-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d46-108">*format*</span><span class="sxs-lookup"><span data-stu-id="71d46-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="71d46-109">Cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="71d46-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="71d46-110">*argumento...*</span><span class="sxs-lookup"><span data-stu-id="71d46-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="71d46-111">Argumentos opcionales.</span><span class="sxs-lookup"><span data-stu-id="71d46-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d46-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71d46-112">Return value</span></span>

<span data-ttu-id="71d46-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="71d46-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d46-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71d46-114">Remarks</span></span>

<span data-ttu-id="71d46-115">Esta operación no hace nada en los dispositivos que no lo admiten.</span><span class="sxs-lookup"><span data-stu-id="71d46-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="71d46-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="71d46-116">Minimum Shader Model</span></span>

<span data-ttu-id="71d46-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="71d46-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71d46-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="71d46-118">Shader Model</span></span>                                                        | <span data-ttu-id="71d46-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="71d46-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="71d46-120">Shader Model 4 (DirectX HLSL) o posterior.</span><span class="sxs-lookup"><span data-stu-id="71d46-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="71d46-121">sí</span><span class="sxs-lookup"><span data-stu-id="71d46-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71d46-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="71d46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d46-123">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="71d46-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




