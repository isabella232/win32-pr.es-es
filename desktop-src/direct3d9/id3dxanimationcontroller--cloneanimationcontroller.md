---
description: Clona o copia un controlador de animación.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'ID3DXAnimationController:: CloneAnimationController (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362759"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="50eea-103">ID3DXAnimationController:: CloneAnimationController (método)</span><span class="sxs-lookup"><span data-stu-id="50eea-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="50eea-104">Clona o copia un controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="50eea-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="50eea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50eea-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="50eea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50eea-107">*MaxNumAnimationOutputs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50eea-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50eea-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50eea-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50eea-109">Número máximo de salidas de animación que el controlador puede admitir.</span><span class="sxs-lookup"><span data-stu-id="50eea-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="50eea-110">*MaxNumAnimationSets* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50eea-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50eea-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50eea-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50eea-112">Número máximo de conjuntos de animaciones que el controlador puede admitir.</span><span class="sxs-lookup"><span data-stu-id="50eea-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="50eea-113">*MaxNumTracks* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50eea-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50eea-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50eea-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50eea-115">Número máximo de pistas que el controlador puede admitir.</span><span class="sxs-lookup"><span data-stu-id="50eea-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="50eea-116">*MaxNumEvents* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50eea-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50eea-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50eea-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50eea-118">Número máximo de eventos que el controlador puede admitir.</span><span class="sxs-lookup"><span data-stu-id="50eea-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="50eea-119">*ppAnimController* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50eea-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50eea-120">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="50eea-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="50eea-121">Dirección de un puntero al controlador de animación [**ID3DXAnimationController**](id3dxanimationcontroller.md) clonado.</span><span class="sxs-lookup"><span data-stu-id="50eea-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50eea-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50eea-122">Return value</span></span>

<span data-ttu-id="50eea-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50eea-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50eea-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50eea-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="50eea-125">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="50eea-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="50eea-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50eea-126">Requirements</span></span>



| <span data-ttu-id="50eea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="50eea-127">Requirement</span></span> | <span data-ttu-id="50eea-128">Value</span><span class="sxs-lookup"><span data-stu-id="50eea-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50eea-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50eea-129">Header</span></span><br/>  | <dl> <span data-ttu-id="50eea-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="50eea-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="50eea-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50eea-131">Library</span></span><br/> | <dl> <span data-ttu-id="50eea-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50eea-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50eea-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="50eea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50eea-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="50eea-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
