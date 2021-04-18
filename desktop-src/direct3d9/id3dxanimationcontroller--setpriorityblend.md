---
description: Establece el peso de fusión de la prioridad usado por el controlador de animación.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController:: SetPriorityBlend (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718410"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="d4c2f-103">ID3DXAnimationController:: SetPriorityBlend (método)</span><span class="sxs-lookup"><span data-stu-id="d4c2f-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="d4c2f-104">Establece el peso de fusión de la prioridad usado por el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="d4c2f-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c2f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4c2f-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="d4c2f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4c2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c2f-107">*BlendWeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4c2f-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c2f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4c2f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4c2f-109">Peso de fusión de prioridad usado por el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="d4c2f-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c2f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4c2f-110">Return value</span></span>

<span data-ttu-id="d4c2f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4c2f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4c2f-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4c2f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4c2f-113">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d4c2f-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c2f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4c2f-114">Remarks</span></span>

<span data-ttu-id="d4c2f-115">El peso de la mezcla se usa para fusionar las pistas de prioridad alta y baja.</span><span class="sxs-lookup"><span data-stu-id="d4c2f-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c2f-116">Requirements</span></span>



| <span data-ttu-id="d4c2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c2f-117">Requirement</span></span> | <span data-ttu-id="d4c2f-118">Value</span><span class="sxs-lookup"><span data-stu-id="d4c2f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c2f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4c2f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d4c2f-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c2f-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d4c2f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4c2f-121">Library</span></span><br/> | <dl> <span data-ttu-id="d4c2f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4c2f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4c2f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4c2f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c2f-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d4c2f-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="d4c2f-125">**GetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="d4c2f-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
