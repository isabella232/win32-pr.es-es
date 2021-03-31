---
description: Rellena una matriz con datos de clave de rotación utilizados para la animación de fotogramas clave.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'ID3DXKeyframedAnimationSet:: GetRotationKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821434"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="11e47-103">ID3DXKeyframedAnimationSet:: GetRotationKeys (método)</span><span class="sxs-lookup"><span data-stu-id="11e47-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="11e47-104">Rellena una matriz con datos de clave de rotación utilizados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="11e47-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11e47-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="11e47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11e47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e47-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="11e47-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e47-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11e47-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11e47-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="11e47-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="11e47-110">*pRotationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11e47-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e47-111">Tipo: **[ **LPD3DXKEY \_ cuaternión**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="11e47-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="11e47-112">Puntero a una matriz asignada por el usuario de los cuaterniones [**D3DXKEY \_ cuaternión**](d3dxkey-quaternion.md) que el método va a rellenar con datos de rotación de animación.</span><span class="sxs-lookup"><span data-stu-id="11e47-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e47-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11e47-113">Return value</span></span>

<span data-ttu-id="11e47-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11e47-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11e47-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11e47-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="11e47-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="11e47-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e47-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11e47-117">Requirements</span></span>



| <span data-ttu-id="11e47-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e47-118">Requirement</span></span> | <span data-ttu-id="11e47-119">Value</span><span class="sxs-lookup"><span data-stu-id="11e47-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11e47-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11e47-120">Header</span></span><br/>  | <dl> <span data-ttu-id="11e47-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e47-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="11e47-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11e47-122">Library</span></span><br/> | <dl> <span data-ttu-id="11e47-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e47-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11e47-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="11e47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e47-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="11e47-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="11e47-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="11e47-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
