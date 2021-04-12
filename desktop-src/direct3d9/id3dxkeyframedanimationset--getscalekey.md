---
description: Obtiene la información de escala de un fotograma clave específico en el conjunto de animaciones.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'ID3DXKeyframedAnimationSet:: GetScaleKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58cbd432404fcd511140a7368999161f5e44f77f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362744"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a><span data-ttu-id="210a5-103">ID3DXKeyframedAnimationSet:: GetScaleKey (método)</span><span class="sxs-lookup"><span data-stu-id="210a5-103">ID3DXKeyframedAnimationSet::GetScaleKey method</span></span>

<span data-ttu-id="210a5-104">Obtiene la información de escala de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="210a5-104">Get scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="210a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="210a5-105">Syntax</span></span>


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="210a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="210a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="210a5-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="210a5-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="210a5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="210a5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="210a5-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="210a5-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="210a5-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="210a5-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="210a5-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="210a5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="210a5-112">Fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="210a5-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="210a5-113">*pScaleKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="210a5-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="210a5-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="210a5-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="210a5-115">Puntero a los datos de la escala.</span><span class="sxs-lookup"><span data-stu-id="210a5-115">Pointer to the scale data.</span></span> <span data-ttu-id="210a5-116">Vea [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="210a5-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="210a5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="210a5-117">Return value</span></span>

<span data-ttu-id="210a5-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="210a5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="210a5-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="210a5-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="210a5-120">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="210a5-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="210a5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="210a5-121">Requirements</span></span>



| <span data-ttu-id="210a5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="210a5-122">Requirement</span></span> | <span data-ttu-id="210a5-123">Value</span><span class="sxs-lookup"><span data-stu-id="210a5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="210a5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="210a5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="210a5-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="210a5-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="210a5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="210a5-126">Library</span></span><br/> | <dl> <span data-ttu-id="210a5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="210a5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="210a5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="210a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210a5-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="210a5-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
