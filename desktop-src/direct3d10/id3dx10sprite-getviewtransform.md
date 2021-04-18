---
description: Obtiene la transformación de la vista que se aplica a todos los sprites.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'ID3DX10Sprite:: GetViewTransform (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718559"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="bd3a7-103">ID3DX10Sprite:: GetViewTransform (método)</span><span class="sxs-lookup"><span data-stu-id="bd3a7-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="bd3a7-104">Obtiene la transformación de la vista que se aplica a todos los sprites.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd3a7-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="bd3a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd3a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd3a7-107">*pViewTransform* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bd3a7-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3a7-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd3a7-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bd3a7-109">Puntero a un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que se establecerá en la transformación del Sprite a partir del espacio universal original.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd3a7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd3a7-110">Return value</span></span>

<span data-ttu-id="bd3a7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd3a7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd3a7-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bd3a7-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bd3a7-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd3a7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd3a7-114">Requirements</span></span>



| <span data-ttu-id="bd3a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd3a7-115">Requirement</span></span> | <span data-ttu-id="bd3a7-116">Value</span><span class="sxs-lookup"><span data-stu-id="bd3a7-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3a7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd3a7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bd3a7-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd3a7-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd3a7-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd3a7-119">Library</span></span><br/> | <dl> <span data-ttu-id="bd3a7-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd3a7-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd3a7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd3a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3a7-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="bd3a7-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="bd3a7-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bd3a7-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
