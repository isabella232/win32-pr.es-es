---
description: Registre los datos del fotograma clave de escala, rotación y traducción (SRT) de una animación.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718463"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="37ea2-103">ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys (método)</span><span class="sxs-lookup"><span data-stu-id="37ea2-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="37ea2-104">Registre los datos del fotograma clave de escala, rotación y traducción (SRT) de una animación.</span><span class="sxs-lookup"><span data-stu-id="37ea2-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ea2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37ea2-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="37ea2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37ea2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ea2-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37ea2-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37ea2-109">Puntero al nombre de la animación.</span><span class="sxs-lookup"><span data-stu-id="37ea2-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-110">*NumScaleKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37ea2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37ea2-112">Número de claves de escala.</span><span class="sxs-lookup"><span data-stu-id="37ea2-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-113">*NumRotationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37ea2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37ea2-115">Número de claves de rotación.</span><span class="sxs-lookup"><span data-stu-id="37ea2-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-116">*NumTranslationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37ea2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37ea2-118">Número de claves de traducción.</span><span class="sxs-lookup"><span data-stu-id="37ea2-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-119">*pScaleKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-120">Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37ea2-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="37ea2-121">Dirección de un puntero a una matriz asignada por el usuario de vectores de [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método rellena con datos de escala.</span><span class="sxs-lookup"><span data-stu-id="37ea2-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-122">*pRotationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-123">Tipo: **const [**LPD3DXKEY \_ cuaternión**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="37ea2-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="37ea2-124">Dirección de un puntero a una matriz asignada por el usuario de los cuaterniones [**D3DXKEY \_ cuaternión**](d3dxkey-quaternion.md) que el método rellena con datos de rotación.</span><span class="sxs-lookup"><span data-stu-id="37ea2-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-125">*pTranslationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-126">Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37ea2-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="37ea2-127">Dirección de un puntero a una matriz asignada por el usuario de vectores de [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método rellena con datos de traducción.</span><span class="sxs-lookup"><span data-stu-id="37ea2-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="37ea2-128">*pAnimationIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="37ea2-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea2-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="37ea2-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="37ea2-130">Devuelve el índice de animación.</span><span class="sxs-lookup"><span data-stu-id="37ea2-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ea2-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37ea2-131">Return value</span></span>

<span data-ttu-id="37ea2-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37ea2-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37ea2-133">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="37ea2-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="37ea2-134">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="37ea2-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="37ea2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37ea2-135">Requirements</span></span>



| <span data-ttu-id="37ea2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="37ea2-136">Requirement</span></span> | <span data-ttu-id="37ea2-137">Value</span><span class="sxs-lookup"><span data-stu-id="37ea2-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ea2-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37ea2-138">Header</span></span><br/>  | <dl> <span data-ttu-id="37ea2-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="37ea2-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="37ea2-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37ea2-140">Library</span></span><br/> | <dl> <span data-ttu-id="37ea2-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37ea2-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37ea2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="37ea2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ea2-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="37ea2-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="37ea2-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="37ea2-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="37ea2-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="37ea2-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="37ea2-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="37ea2-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
