---
description: Rellena una matriz con los datos de clave de escala que se usan para la animación de fotogramas clave.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet:: GetScaleKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718469"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a><span data-ttu-id="59b44-103">ID3DXKeyframedAnimationSet:: GetScaleKeys (método)</span><span class="sxs-lookup"><span data-stu-id="59b44-103">ID3DXKeyframedAnimationSet::GetScaleKeys method</span></span>

<span data-ttu-id="59b44-104">Rellena una matriz con los datos de clave de escala que se usan para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="59b44-104">Fills an array with scale key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b44-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59b44-105">Syntax</span></span>


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="59b44-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b44-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="59b44-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b44-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59b44-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59b44-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="59b44-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="59b44-110">*pScaleKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b44-110">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b44-111">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="59b44-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="59b44-112">Puntero a una matriz asignada por el usuario de vectores de [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método va a rellenar con datos de escala de animación.</span><span class="sxs-lookup"><span data-stu-id="59b44-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation scale data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b44-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b44-113">Return value</span></span>

<span data-ttu-id="59b44-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59b44-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59b44-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59b44-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59b44-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="59b44-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b44-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b44-117">Requirements</span></span>



| <span data-ttu-id="59b44-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b44-118">Requirement</span></span> | <span data-ttu-id="59b44-119">Value</span><span class="sxs-lookup"><span data-stu-id="59b44-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59b44-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59b44-120">Header</span></span><br/>  | <dl> <span data-ttu-id="59b44-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b44-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="59b44-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59b44-122">Library</span></span><br/> | <dl> <span data-ttu-id="59b44-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59b44-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59b44-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="59b44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b44-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="59b44-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="59b44-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="59b44-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
