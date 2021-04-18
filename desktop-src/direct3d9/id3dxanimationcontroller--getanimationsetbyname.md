---
description: Obtiene un conjunto de animaciones, dado su nombre.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController:: GetAnimationSetByName (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718377"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="23f1d-103">ID3DXAnimationController:: GetAnimationSetByName (método)</span><span class="sxs-lookup"><span data-stu-id="23f1d-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="23f1d-104">Obtiene un conjunto de animaciones, dado su nombre.</span><span class="sxs-lookup"><span data-stu-id="23f1d-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23f1d-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="23f1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23f1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f1d-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23f1d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f1d-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23f1d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23f1d-109">Cadena que contiene el nombre del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="23f1d-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="23f1d-110">*ppAnimSet* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23f1d-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23f1d-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="23f1d-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="23f1d-112">Puntero al conjunto de animaciones [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="23f1d-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f1d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23f1d-113">Return value</span></span>

<span data-ttu-id="23f1d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23f1d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23f1d-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23f1d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="23f1d-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="23f1d-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f1d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23f1d-117">Remarks</span></span>

<span data-ttu-id="23f1d-118">El controlador de animación contiene una matriz de conjuntos de animaciones.</span><span class="sxs-lookup"><span data-stu-id="23f1d-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="23f1d-119">Este método devuelve un conjunto de animaciones que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="23f1d-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f1d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f1d-120">Requirements</span></span>



| <span data-ttu-id="23f1d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f1d-121">Requirement</span></span> | <span data-ttu-id="23f1d-122">Value</span><span class="sxs-lookup"><span data-stu-id="23f1d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23f1d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23f1d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="23f1d-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f1d-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="23f1d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23f1d-125">Library</span></span><br/> | <dl> <span data-ttu-id="23f1d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23f1d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23f1d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="23f1d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f1d-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="23f1d-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
