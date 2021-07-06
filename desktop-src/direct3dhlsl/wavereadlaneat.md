---
title: Función WaveReadLaneAt
description: Devuelve el valor de la expresión para el índice de la cadena especificado dentro de la onda especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Función HLSL de WaveReadLaneAt
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316487"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="0bbce-104">Función WaveReadLaneAt</span><span class="sxs-lookup"><span data-stu-id="0bbce-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="0bbce-105">Devuelve el valor de la expresión para el índice de la cadena especificado dentro de la onda especificada.</span><span class="sxs-lookup"><span data-stu-id="0bbce-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbce-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bbce-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="0bbce-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bbce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bbce-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="0bbce-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0bbce-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="0bbce-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="0bbce-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="0bbce-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="0bbce-111">Índice del lane para el que se devolverá el resultado *expr.*</span><span class="sxs-lookup"><span data-stu-id="0bbce-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bbce-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bbce-112">Return value</span></span>

<span data-ttu-id="0bbce-113">El valor resultante es el resultado de *expr*.</span><span class="sxs-lookup"><span data-stu-id="0bbce-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="0bbce-114">Será uniforme si *laneIndex* es uniforme.</span><span class="sxs-lookup"><span data-stu-id="0bbce-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bbce-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0bbce-115">Remarks</span></span>

<span data-ttu-id="0bbce-116">Esta función es efectivamente una difusión del valor en *el laneIndex*'th lane.</span><span class="sxs-lookup"><span data-stu-id="0bbce-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="0bbce-117">Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="0bbce-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bbce-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0bbce-118">See also</span></span>

* [<span data-ttu-id="0bbce-119">Información general del modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="0bbce-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="0bbce-120">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="0bbce-120">Shader Model 6</span></span>](shader-model-6-0.md)
