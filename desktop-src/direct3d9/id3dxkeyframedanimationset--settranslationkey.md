---
description: Establezca la información de traducción de un fotograma clave específico en el conjunto de animaciones.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'ID3DXKeyframedAnimationSet:: SetTranslationKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718460"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a><span data-ttu-id="ba6ac-103">ID3DXKeyframedAnimationSet:: SetTranslationKey (método)</span><span class="sxs-lookup"><span data-stu-id="ba6ac-103">ID3DXKeyframedAnimationSet::SetTranslationKey method</span></span>

<span data-ttu-id="ba6ac-104">Establezca la información de traducción de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-104">Set translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba6ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba6ac-105">Syntax</span></span>


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="ba6ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba6ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba6ac-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ba6ac-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba6ac-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba6ac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba6ac-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="ba6ac-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ba6ac-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba6ac-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba6ac-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba6ac-112">Fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="ba6ac-113">*pTranslationKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba6ac-113">*pTranslationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba6ac-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="ba6ac-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="ba6ac-115">Puntero a los datos de traducción.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-115">Pointer to the translation data.</span></span> <span data-ttu-id="ba6ac-116">Vea [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="ba6ac-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba6ac-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba6ac-117">Return value</span></span>

<span data-ttu-id="ba6ac-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba6ac-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba6ac-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ba6ac-120">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ba6ac-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba6ac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba6ac-121">Requirements</span></span>



| <span data-ttu-id="ba6ac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba6ac-122">Requirement</span></span> | <span data-ttu-id="ba6ac-123">Value</span><span class="sxs-lookup"><span data-stu-id="ba6ac-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba6ac-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba6ac-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ba6ac-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba6ac-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ba6ac-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba6ac-126">Library</span></span><br/> | <dl> <span data-ttu-id="ba6ac-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba6ac-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba6ac-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba6ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6ac-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="ba6ac-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
