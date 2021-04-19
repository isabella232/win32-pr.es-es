---
description: Obtiene el período del conjunto de animaciones.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet:: GetPeriod (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698419"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="35c20-103">ID3DXAnimationSet:: GetPeriod (método)</span><span class="sxs-lookup"><span data-stu-id="35c20-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="35c20-104">Obtiene el período del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="35c20-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35c20-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="35c20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35c20-106">Parameters</span></span>

<span data-ttu-id="35c20-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="35c20-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35c20-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35c20-108">Return value</span></span>

<span data-ttu-id="35c20-109">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35c20-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35c20-110">Período del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="35c20-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c20-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35c20-111">Remarks</span></span>

<span data-ttu-id="35c20-112">El período es el intervalo de tiempo en el que los fotogramas clave de la animación son válidos.</span><span class="sxs-lookup"><span data-stu-id="35c20-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="35c20-113">En el caso de las animaciones de bucle, este es el período del bucle.</span><span class="sxs-lookup"><span data-stu-id="35c20-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="35c20-114">La aplicación determina las unidades de tiempo en las que se especifican los fotogramas clave (por ejemplo, segundos).</span><span class="sxs-lookup"><span data-stu-id="35c20-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c20-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35c20-115">Requirements</span></span>



| <span data-ttu-id="35c20-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c20-116">Requirement</span></span> | <span data-ttu-id="35c20-117">Value</span><span class="sxs-lookup"><span data-stu-id="35c20-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35c20-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35c20-118">Header</span></span><br/>  | <dl> <span data-ttu-id="35c20-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="35c20-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="35c20-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35c20-120">Library</span></span><br/> | <dl> <span data-ttu-id="35c20-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35c20-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35c20-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="35c20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c20-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="35c20-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
