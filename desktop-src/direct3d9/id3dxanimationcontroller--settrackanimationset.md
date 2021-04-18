---
description: Aplica la animación establecida a la pista especificada.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController:: SetTrackAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718409"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="0f64d-103">ID3DXAnimationController:: SetTrackAnimationSet (método)</span><span class="sxs-lookup"><span data-stu-id="0f64d-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="0f64d-104">Aplica la animación establecida a la pista especificada.</span><span class="sxs-lookup"><span data-stu-id="0f64d-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f64d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f64d-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="0f64d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f64d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f64d-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f64d-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f64d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f64d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f64d-109">Identificador de la pista a la que se aplica el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="0f64d-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="0f64d-110">*pAnimSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f64d-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f64d-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="0f64d-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="0f64d-112">Puntero al conjunto de animaciones [**ID3DXAnimationSet**](id3dxanimationset.md) que se va a agregar a la pista.</span><span class="sxs-lookup"><span data-stu-id="0f64d-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f64d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f64d-113">Return value</span></span>

<span data-ttu-id="0f64d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f64d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f64d-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f64d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0f64d-116">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0f64d-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f64d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f64d-117">Remarks</span></span>

<span data-ttu-id="0f64d-118">Este método establece la animación establecida en la pista especificada para la combinación.</span><span class="sxs-lookup"><span data-stu-id="0f64d-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="0f64d-119">El conjunto de animación de cada pista se combina según el peso y la velocidad del seguimiento cuando se llama a [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .</span><span class="sxs-lookup"><span data-stu-id="0f64d-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f64d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f64d-120">Requirements</span></span>



| <span data-ttu-id="0f64d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f64d-121">Requirement</span></span> | <span data-ttu-id="0f64d-122">Value</span><span class="sxs-lookup"><span data-stu-id="0f64d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f64d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f64d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0f64d-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f64d-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0f64d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f64d-125">Library</span></span><br/> | <dl> <span data-ttu-id="0f64d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f64d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f64d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f64d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f64d-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="0f64d-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
