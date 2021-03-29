---
description: Quita los datos de traducción en el fotograma clave especificado.
ms.assetid: 58cadf5d-f687-4644-83b0-e124ef2bcb5a
title: 'ID3DXKeyframedAnimationSet:: UnregisterTranslationKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 127aaa707c364e51815af09b8222d73102281b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678849"
---
# <a name="id3dxkeyframedanimationsetunregistertranslationkey-method"></a><span data-ttu-id="2fe5b-103">ID3DXKeyframedAnimationSet:: UnregisterTranslationKey (método)</span><span class="sxs-lookup"><span data-stu-id="2fe5b-103">ID3DXKeyframedAnimationSet::UnregisterTranslationKey method</span></span>

<span data-ttu-id="2fe5b-104">Quita los datos de traducción en el fotograma clave especificado.</span><span class="sxs-lookup"><span data-stu-id="2fe5b-104">Removes the translation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe5b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fe5b-105">Syntax</span></span>


```C++
HRESULT UnregisterTranslationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="2fe5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fe5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe5b-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2fe5b-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe5b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fe5b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fe5b-109">Identificador de animación.</span><span class="sxs-lookup"><span data-stu-id="2fe5b-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2fe5b-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2fe5b-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe5b-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fe5b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fe5b-112">Fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="2fe5b-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe5b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fe5b-113">Return value</span></span>

<span data-ttu-id="2fe5b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fe5b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fe5b-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2fe5b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2fe5b-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2fe5b-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fe5b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fe5b-117">Remarks</span></span>

<span data-ttu-id="2fe5b-118">Este método es lento y no debe usarse una vez iniciada la reproducción de una animación.</span><span class="sxs-lookup"><span data-stu-id="2fe5b-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe5b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fe5b-119">Requirements</span></span>



| <span data-ttu-id="2fe5b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fe5b-120">Requirement</span></span> | <span data-ttu-id="2fe5b-121">Value</span><span class="sxs-lookup"><span data-stu-id="2fe5b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe5b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fe5b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2fe5b-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fe5b-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2fe5b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fe5b-124">Library</span></span><br/> | <dl> <span data-ttu-id="2fe5b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fe5b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2fe5b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fe5b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe5b-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="2fe5b-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
