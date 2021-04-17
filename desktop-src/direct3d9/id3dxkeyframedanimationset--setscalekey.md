---
description: Establezca la información de escala para un fotograma clave específico en el conjunto de animaciones.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: 'ID3DXKeyframedAnimationSet:: SetScaleKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12ac4d46a2719e452d44d2da67f178e6146b799b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718461"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a><span data-ttu-id="e3b91-103">ID3DXKeyframedAnimationSet:: SetScaleKey (método)</span><span class="sxs-lookup"><span data-stu-id="e3b91-103">ID3DXKeyframedAnimationSet::SetScaleKey method</span></span>

<span data-ttu-id="e3b91-104">Establezca la información de escala para un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="e3b91-104">Set scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b91-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3b91-105">Syntax</span></span>


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="e3b91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3b91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b91-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3b91-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b91-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b91-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b91-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="e3b91-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="e3b91-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3b91-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b91-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b91-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b91-112">Fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="e3b91-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="e3b91-113">*pScaleKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3b91-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b91-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b91-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="e3b91-115">Puntero a los datos de la escala.</span><span class="sxs-lookup"><span data-stu-id="e3b91-115">Pointer to the scale data.</span></span> <span data-ttu-id="e3b91-116">Vea [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="e3b91-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b91-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3b91-117">Return value</span></span>

<span data-ttu-id="e3b91-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3b91-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3b91-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3b91-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e3b91-120">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e3b91-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b91-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b91-121">Requirements</span></span>



| <span data-ttu-id="e3b91-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b91-122">Requirement</span></span> | <span data-ttu-id="e3b91-123">Value</span><span class="sxs-lookup"><span data-stu-id="e3b91-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b91-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b91-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b91-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b91-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b91-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3b91-126">Library</span></span><br/> | <dl> <span data-ttu-id="e3b91-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b91-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3b91-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3b91-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b91-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e3b91-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
