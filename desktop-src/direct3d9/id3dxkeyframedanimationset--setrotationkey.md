---
description: Establezca la información de rotación de un fotograma clave específico en el conjunto de animaciones.
ms.assetid: b31edc88-0d77-49f3-b4c4-39cd866e1379
title: 'ID3DXKeyframedAnimationSet:: SetRotationKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b03a6818a6a59904c3db5b4819775d9e58d4f8ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083794"
---
# <a name="id3dxkeyframedanimationsetsetrotationkey-method"></a><span data-ttu-id="87fa6-103">ID3DXKeyframedAnimationSet:: SetRotationKey (método)</span><span class="sxs-lookup"><span data-stu-id="87fa6-103">ID3DXKeyframedAnimationSet::SetRotationKey method</span></span>

<span data-ttu-id="87fa6-104">Establezca la información de rotación de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="87fa6-104">Set rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fa6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87fa6-105">Syntax</span></span>


```C++
HRESULT SetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="87fa6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87fa6-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="87fa6-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87fa6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87fa6-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="87fa6-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="87fa6-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87fa6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87fa6-112">Fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="87fa6-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="87fa6-113">*pRotationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87fa6-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87fa6-114">Tipo: **[ **LPD3DXKEY \_ cuaternión**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="87fa6-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="87fa6-115">Puntero a los datos de rotación.</span><span class="sxs-lookup"><span data-stu-id="87fa6-115">Pointer to the rotation data.</span></span> <span data-ttu-id="87fa6-116">Vea [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="87fa6-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87fa6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87fa6-117">Return value</span></span>

<span data-ttu-id="87fa6-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87fa6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87fa6-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87fa6-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="87fa6-120">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="87fa6-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fa6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87fa6-121">Requirements</span></span>



| <span data-ttu-id="87fa6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="87fa6-122">Requirement</span></span> | <span data-ttu-id="87fa6-123">Value</span><span class="sxs-lookup"><span data-stu-id="87fa6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87fa6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87fa6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="87fa6-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="87fa6-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="87fa6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87fa6-126">Library</span></span><br/> | <dl> <span data-ttu-id="87fa6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87fa6-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87fa6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="87fa6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87fa6-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="87fa6-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
