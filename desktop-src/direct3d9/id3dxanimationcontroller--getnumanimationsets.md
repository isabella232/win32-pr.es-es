---
description: Devuelve el número de conjuntos de animación registrados actualmente en el controlador de animación.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController:: GetNumAnimationSets (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717575"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="83593-103">ID3DXAnimationController:: GetNumAnimationSets (método)</span><span class="sxs-lookup"><span data-stu-id="83593-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="83593-104">Devuelve el número de conjuntos de animación registrados actualmente en el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="83593-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="83593-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83593-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="83593-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83593-106">Parameters</span></span>

<span data-ttu-id="83593-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="83593-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83593-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83593-108">Return value</span></span>

<span data-ttu-id="83593-109">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83593-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83593-110">Número de conjuntos de animaciones.</span><span class="sxs-lookup"><span data-stu-id="83593-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="83593-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83593-111">Remarks</span></span>

<span data-ttu-id="83593-112">El controlador contiene cualquier número de conjuntos de animaciones y pistas.</span><span class="sxs-lookup"><span data-stu-id="83593-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="83593-113">Los conjuntos de animaciones se pueden registrar con [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span><span class="sxs-lookup"><span data-stu-id="83593-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="83593-114">Un controlador de animación creado por una llamada a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrará automáticamente los conjuntos de animaciones cargados.</span><span class="sxs-lookup"><span data-stu-id="83593-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="83593-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83593-115">Requirements</span></span>



| <span data-ttu-id="83593-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83593-116">Requirement</span></span> | <span data-ttu-id="83593-117">Value</span><span class="sxs-lookup"><span data-stu-id="83593-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83593-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83593-118">Header</span></span><br/>  | <dl> <span data-ttu-id="83593-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="83593-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="83593-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83593-120">Library</span></span><br/> | <dl> <span data-ttu-id="83593-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83593-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83593-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="83593-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83593-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="83593-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
