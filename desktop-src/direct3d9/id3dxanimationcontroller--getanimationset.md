---
description: Obtiene un conjunto de animaciones.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'ID3DXAnimationController:: GetAnimationSet (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157212"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="5b2bc-103">ID3DXAnimationController:: GetAnimationSet (método)</span><span class="sxs-lookup"><span data-stu-id="5b2bc-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="5b2bc-104">Obtiene un conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b2bc-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="5b2bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b2bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b2bc-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5b2bc-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2bc-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b2bc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b2bc-109">Índice del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="5b2bc-110">*ppAnimSet* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5b2bc-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2bc-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b2bc-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="5b2bc-112">Puntero al conjunto de animaciones [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="5b2bc-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b2bc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b2bc-113">Return value</span></span>

<span data-ttu-id="5b2bc-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b2bc-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b2bc-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5b2bc-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b2bc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b2bc-117">Remarks</span></span>

<span data-ttu-id="5b2bc-118">El controlador de animación contiene una matriz de conjuntos de animaciones.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="5b2bc-119">Este método devuelve uno de ellos en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5b2bc-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2bc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b2bc-120">Requirements</span></span>



| <span data-ttu-id="5b2bc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2bc-121">Requirement</span></span> | <span data-ttu-id="5b2bc-122">Value</span><span class="sxs-lookup"><span data-stu-id="5b2bc-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2bc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b2bc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5b2bc-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b2bc-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5b2bc-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b2bc-125">Library</span></span><br/> | <dl> <span data-ttu-id="5b2bc-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b2bc-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b2bc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b2bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2bc-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="5b2bc-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
