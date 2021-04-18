---
description: Establece el peso de fusión de prioridad para la pista de animación especificada.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController:: SetTrackPriority (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718533"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="b552c-103">ID3DXAnimationController:: SetTrackPriority (método)</span><span class="sxs-lookup"><span data-stu-id="b552c-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="b552c-104">Establece el peso de fusión de prioridad para la pista de animación especificada.</span><span class="sxs-lookup"><span data-stu-id="b552c-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="b552c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b552c-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="b552c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b552c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b552c-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b552c-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b552c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b552c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b552c-109">Identificador de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b552c-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b552c-110">*Prioridad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b552c-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b552c-111">Tipo: **[ **D3DXPRIORITY \_ Type**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b552c-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="b552c-112">Prioridad de la pista.</span><span class="sxs-lookup"><span data-stu-id="b552c-112">Track priority.</span></span> <span data-ttu-id="b552c-113">Este parámetro debe establecerse en una de las constantes de [**\_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="b552c-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b552c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b552c-114">Return value</span></span>

<span data-ttu-id="b552c-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b552c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b552c-116">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b552c-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b552c-117">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b552c-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b552c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b552c-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b552c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b552c-119">Requirements</span></span>



| <span data-ttu-id="b552c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b552c-120">Requirement</span></span> | <span data-ttu-id="b552c-121">Value</span><span class="sxs-lookup"><span data-stu-id="b552c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b552c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b552c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b552c-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b552c-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b552c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b552c-124">Library</span></span><br/> | <dl> <span data-ttu-id="b552c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b552c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b552c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b552c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b552c-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b552c-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
