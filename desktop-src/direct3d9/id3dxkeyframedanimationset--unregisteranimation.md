---
description: Quitar los datos de animación del conjunto de animaciones.
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'ID3DXKeyframedAnimationSet:: UnregisterAnimation (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721547"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a><span data-ttu-id="a3f8f-103">ID3DXKeyframedAnimationSet:: UnregisterAnimation (método)</span><span class="sxs-lookup"><span data-stu-id="a3f8f-103">ID3DXKeyframedAnimationSet::UnregisterAnimation method</span></span>

<span data-ttu-id="a3f8f-104">Quitar los datos de animación del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-104">Remove the animation data from the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3f8f-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="a3f8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f8f-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a3f8f-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f8f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3f8f-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-109">The animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f8f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3f8f-110">Return value</span></span>

<span data-ttu-id="a3f8f-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3f8f-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a3f8f-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f8f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3f8f-114">Requirements</span></span>



| <span data-ttu-id="a3f8f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f8f-115">Requirement</span></span> | <span data-ttu-id="a3f8f-116">Value</span><span class="sxs-lookup"><span data-stu-id="a3f8f-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f8f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3f8f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f8f-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f8f-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a3f8f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3f8f-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3f8f-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3f8f-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3f8f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3f8f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f8f-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a3f8f-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
