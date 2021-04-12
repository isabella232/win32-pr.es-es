---
description: Devuelve la posición de hora en el intervalo de tiempo local de un conjunto de animaciones.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet:: GetPeriodicPosition (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362786"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="1d646-103">ID3DXAnimationSet:: GetPeriodicPosition (método)</span><span class="sxs-lookup"><span data-stu-id="1d646-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="1d646-104">Devuelve la posición de hora en el intervalo de tiempo local de un conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="1d646-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d646-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d646-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="1d646-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d646-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d646-107">*Posición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1d646-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d646-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d646-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d646-109">Hora local del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="1d646-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d646-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d646-110">Return value</span></span>

<span data-ttu-id="1d646-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d646-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d646-112">Posición de hora medida en el período de tiempo del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="1d646-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="1d646-113">Este valor estará limitado por el período del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="1d646-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d646-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d646-114">Remarks</span></span>

<span data-ttu-id="1d646-115">La posición de hora devuelta por este método se puede usar como el parámetro PeriodicPosition de [**ID3DXAnimationSet:: GetSRT**](id3dxanimationset--getsrt.md).</span><span class="sxs-lookup"><span data-stu-id="1d646-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d646-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d646-116">Requirements</span></span>



| <span data-ttu-id="1d646-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d646-117">Requirement</span></span> | <span data-ttu-id="1d646-118">Value</span><span class="sxs-lookup"><span data-stu-id="1d646-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d646-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d646-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1d646-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d646-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1d646-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d646-121">Library</span></span><br/> | <dl> <span data-ttu-id="1d646-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d646-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d646-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d646-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d646-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1d646-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
