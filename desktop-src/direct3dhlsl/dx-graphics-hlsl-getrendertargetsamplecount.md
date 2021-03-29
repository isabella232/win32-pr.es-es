---
title: GetRenderTargetSampleCount
description: Obtiene el número de muestras para un destino de representación.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- HLSL de GetRenderTargetSampleCount
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487162"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="66907-104">GetRenderTargetSampleCount</span><span class="sxs-lookup"><span data-stu-id="66907-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="66907-105">Obtiene el número de muestras para un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="66907-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="66907-106">*Uint* GetRenderTargetSampleCount()</span><span class="sxs-lookup"><span data-stu-id="66907-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="66907-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66907-107">Parameters</span></span>



| <span data-ttu-id="66907-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="66907-108">Item</span></span>                                                                                 | <span data-ttu-id="66907-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="66907-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="66907-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>Ninguna</span><span class="sxs-lookup"><span data-stu-id="66907-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="66907-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66907-111">Return Value</span></span>

<span data-ttu-id="66907-112">Número de muestras.</span><span class="sxs-lookup"><span data-stu-id="66907-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="66907-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66907-113">Remarks</span></span>

<span data-ttu-id="66907-114">Use esta función y [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) para averiguar el número y la posición de las ubicaciones de muestreo para un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="66907-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="66907-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="66907-115">Minimum Shader Model</span></span>

<span data-ttu-id="66907-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="66907-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="66907-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="66907-117">Shader Model</span></span>                                                        | <span data-ttu-id="66907-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="66907-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="66907-119">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="66907-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="66907-120">sí</span><span class="sxs-lookup"><span data-stu-id="66907-120">yes</span></span>       |
| [<span data-ttu-id="66907-121">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66907-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="66907-122">no</span><span class="sxs-lookup"><span data-stu-id="66907-122">no</span></span>        |
| [<span data-ttu-id="66907-123">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66907-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="66907-124">no</span><span class="sxs-lookup"><span data-stu-id="66907-124">no</span></span>        |
| [<span data-ttu-id="66907-125">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="66907-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="66907-126">No</span><span class="sxs-lookup"><span data-stu-id="66907-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="66907-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="66907-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66907-128">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="66907-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





