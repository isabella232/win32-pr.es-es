---
description: Rellena una matriz con datos de clave de traducción usados para la animación de fotogramas clave.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'ID3DXKeyframedAnimationSet:: GetTranslationKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6cc56e5538eb45c01ba7c35115e94719119bc4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718466"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a><span data-ttu-id="9c81b-103">ID3DXKeyframedAnimationSet:: GetTranslationKeys (método)</span><span class="sxs-lookup"><span data-stu-id="9c81b-103">ID3DXKeyframedAnimationSet::GetTranslationKeys method</span></span>

<span data-ttu-id="9c81b-104">Rellena una matriz con datos de clave de traducción usados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="9c81b-104">Fills an array with translational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c81b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c81b-105">Syntax</span></span>


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="9c81b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c81b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c81b-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9c81b-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c81b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c81b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c81b-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="9c81b-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="9c81b-110">*pTranslationKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c81b-110">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c81b-111">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="9c81b-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="9c81b-112">Puntero a una matriz asignada por el usuario de vectores de [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método va a rellenar con datos de traducción de animaciones.</span><span class="sxs-lookup"><span data-stu-id="9c81b-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation translation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c81b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c81b-113">Return value</span></span>

<span data-ttu-id="9c81b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c81b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c81b-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c81b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9c81b-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9c81b-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c81b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c81b-117">Requirements</span></span>



| <span data-ttu-id="9c81b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c81b-118">Requirement</span></span> | <span data-ttu-id="9c81b-119">Value</span><span class="sxs-lookup"><span data-stu-id="9c81b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c81b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c81b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9c81b-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c81b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9c81b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c81b-122">Library</span></span><br/> | <dl> <span data-ttu-id="9c81b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c81b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c81b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c81b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c81b-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="9c81b-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="9c81b-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="9c81b-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
