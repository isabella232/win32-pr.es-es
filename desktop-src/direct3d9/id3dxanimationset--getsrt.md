---
description: Obtiene los valores de escala, rotación y traslación del conjunto de animaciones.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet:: GetSRT (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718521"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="276aa-103">ID3DXAnimationSet:: GetSRT (método)</span><span class="sxs-lookup"><span data-stu-id="276aa-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="276aa-104">Obtiene los valores de escala, rotación y traslación del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="276aa-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="276aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="276aa-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="276aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="276aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276aa-107">*PeriodicPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="276aa-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276aa-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="276aa-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="276aa-109">Posición del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="276aa-109">Position of the animation set.</span></span> <span data-ttu-id="276aa-110">La posición se puede obtener llamando a [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span><span class="sxs-lookup"><span data-stu-id="276aa-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="276aa-111">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="276aa-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276aa-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="276aa-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="276aa-113">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="276aa-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="276aa-114">*pScale* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="276aa-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="276aa-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="276aa-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="276aa-116">Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la escala del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="276aa-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="276aa-117">*Prot.* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="276aa-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="276aa-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="276aa-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="276aa-119">Puntero al cuaternión [**D3DXQUATERNION**](d3dxquaternion.md) que describe el giro del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="276aa-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="276aa-120">*pTranslation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="276aa-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="276aa-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="276aa-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="276aa-122">Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traslación del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="276aa-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276aa-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="276aa-123">Return value</span></span>

<span data-ttu-id="276aa-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="276aa-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="276aa-125">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="276aa-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="276aa-126">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="276aa-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="276aa-127">En caso contrario, programe el método para que devuelva un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="276aa-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="276aa-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="276aa-128">Requirements</span></span>



| <span data-ttu-id="276aa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="276aa-129">Requirement</span></span> | <span data-ttu-id="276aa-130">Value</span><span class="sxs-lookup"><span data-stu-id="276aa-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="276aa-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="276aa-131">Header</span></span><br/>  | <dl> <span data-ttu-id="276aa-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="276aa-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="276aa-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="276aa-133">Library</span></span><br/> | <dl> <span data-ttu-id="276aa-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="276aa-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="276aa-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="276aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276aa-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="276aa-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
