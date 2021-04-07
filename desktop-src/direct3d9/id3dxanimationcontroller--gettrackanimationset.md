---
description: Obtiene el conjunto de animaciones para la pista especificada.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'ID3DXAnimationController:: GetTrackAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003886"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a><span data-ttu-id="ad91e-103">ID3DXAnimationController:: GetTrackAnimationSet (método)</span><span class="sxs-lookup"><span data-stu-id="ad91e-103">ID3DXAnimationController::GetTrackAnimationSet method</span></span>

<span data-ttu-id="ad91e-104">Obtiene el conjunto de animaciones para la pista especificada.</span><span class="sxs-lookup"><span data-stu-id="ad91e-104">Gets the animation set for the given track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad91e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad91e-105">Syntax</span></span>


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="ad91e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad91e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad91e-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ad91e-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad91e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad91e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad91e-109">Identificador de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ad91e-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ad91e-110">*ppAnimSet* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ad91e-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad91e-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad91e-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="ad91e-112">Puntero a la animación [**ID3DXAnimationSet**](id3dxanimationset.md) establecida para la pista especificada.</span><span class="sxs-lookup"><span data-stu-id="ad91e-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set for the given track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad91e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad91e-113">Return value</span></span>

<span data-ttu-id="ad91e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad91e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad91e-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad91e-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ad91e-116">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ad91e-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad91e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad91e-117">Requirements</span></span>



| <span data-ttu-id="ad91e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad91e-118">Requirement</span></span> | <span data-ttu-id="ad91e-119">Value</span><span class="sxs-lookup"><span data-stu-id="ad91e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad91e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad91e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ad91e-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad91e-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ad91e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad91e-122">Library</span></span><br/> | <dl> <span data-ttu-id="ad91e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad91e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad91e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad91e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad91e-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ad91e-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
