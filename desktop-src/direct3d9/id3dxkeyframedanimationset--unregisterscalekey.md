---
description: Quita los datos de escala en el fotograma clave especificado.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'ID3DXKeyframedAnimationSet:: UnregisterScaleKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003956"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a><span data-ttu-id="74a47-103">ID3DXKeyframedAnimationSet:: UnregisterScaleKey (método)</span><span class="sxs-lookup"><span data-stu-id="74a47-103">ID3DXKeyframedAnimationSet::UnregisterScaleKey method</span></span>

<span data-ttu-id="74a47-104">Quita los datos de escala en el fotograma clave especificado.</span><span class="sxs-lookup"><span data-stu-id="74a47-104">Removes the scale data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74a47-105">Syntax</span></span>


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="74a47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74a47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74a47-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="74a47-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a47-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74a47-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74a47-109">Identificador de animación.</span><span class="sxs-lookup"><span data-stu-id="74a47-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="74a47-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="74a47-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74a47-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74a47-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74a47-112">Fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="74a47-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74a47-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74a47-113">Return value</span></span>

<span data-ttu-id="74a47-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74a47-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74a47-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74a47-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="74a47-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="74a47-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="74a47-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74a47-117">Remarks</span></span>

<span data-ttu-id="74a47-118">Este método es lento y no debe usarse una vez iniciada la reproducción de una animación.</span><span class="sxs-lookup"><span data-stu-id="74a47-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="74a47-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74a47-119">Requirements</span></span>



| <span data-ttu-id="74a47-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="74a47-120">Requirement</span></span> | <span data-ttu-id="74a47-121">Value</span><span class="sxs-lookup"><span data-stu-id="74a47-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74a47-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74a47-122">Header</span></span><br/>  | <dl> <span data-ttu-id="74a47-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="74a47-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="74a47-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74a47-124">Library</span></span><br/> | <dl> <span data-ttu-id="74a47-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74a47-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74a47-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="74a47-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a47-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="74a47-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
