---
description: Esta interfaz encapsula la funcionalidad mínima necesaria de una animación establecida por un controlador de animaciones.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interfaz ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280503"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="bdcf2-103">Interfaz ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="bdcf2-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="bdcf2-104">Esta interfaz encapsula la funcionalidad mínima necesaria de una animación establecida por un controlador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="bdcf2-105">Es posible que los usuarios avanzados deseen implementar esta interfaz para satisfacer sus necesidades especializadas. sin embargo, para la mayoría de los usuarios, las interfaces derivadas [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) y [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) deben ser suficientes.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="bdcf2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bdcf2-106">Members</span></span>

<span data-ttu-id="bdcf2-107">La interfaz **ID3DXAnimationSet** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bdcf2-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bdcf2-108">**ID3DXAnimationSet** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bdcf2-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="bdcf2-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="bdcf2-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bdcf2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bdcf2-110">Methods</span></span>

<span data-ttu-id="bdcf2-111">La interfaz **ID3DXAnimationSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="bdcf2-112">Método</span><span class="sxs-lookup"><span data-stu-id="bdcf2-112">Method</span></span>                                                                        | <span data-ttu-id="bdcf2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdcf2-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="bdcf2-114">**GetAnimationIndexByName**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="bdcf2-115">Obtiene el índice de una animación, dado su nombre.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="bdcf2-116">**GetAnimationNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="bdcf2-117">Obtiene el nombre de una animación, según su índice.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="bdcf2-118">**GetCallback**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="bdcf2-119">Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="bdcf2-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="bdcf2-121">Obtiene el nombre del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="bdcf2-122">**GetNumAnimations**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="bdcf2-123">Obtiene el número de animaciones en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="bdcf2-124">**GetPeriod**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="bdcf2-125">Obtiene el período del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="bdcf2-126">**GetPeriodicPosition**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="bdcf2-127">Devuelve la posición de hora en el intervalo de tiempo local de un conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="bdcf2-128">**GetSRT**</span><span class="sxs-lookup"><span data-stu-id="bdcf2-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="bdcf2-129">Obtiene los valores de escala, rotación y traslación del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdcf2-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdcf2-130">Remarks</span></span>

<span data-ttu-id="bdcf2-131">Un conjunto de animaciones consta de animaciones para muchos nodos de la misma animación.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="bdcf2-132">El tipo LPD3DXANIMATIONSET se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="bdcf2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdcf2-133">Requirements</span></span>



| <span data-ttu-id="bdcf2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdcf2-134">Requirement</span></span> | <span data-ttu-id="bdcf2-135">Value</span><span class="sxs-lookup"><span data-stu-id="bdcf2-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcf2-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdcf2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="bdcf2-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdcf2-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bdcf2-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdcf2-138">Library</span></span><br/> | <dl> <span data-ttu-id="bdcf2-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdcf2-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bdcf2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdcf2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcf2-141">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bdcf2-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
