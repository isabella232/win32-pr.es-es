---
description: Establezca la transformación de la vista que se aplica a todos los sprites.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'ID3DX10Sprite:: SetViewTransform (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708125"
---
# <a name="id3dx10spritesetviewtransform-method"></a><span data-ttu-id="bc6a5-103">ID3DX10Sprite:: SetViewTransform (método)</span><span class="sxs-lookup"><span data-stu-id="bc6a5-103">ID3DX10Sprite::SetViewTransform method</span></span>

<span data-ttu-id="bc6a5-104">Establezca la transformación de la vista que se aplica a todos los sprites.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-104">Set the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc6a5-105">Syntax</span></span>


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="bc6a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc6a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc6a5-107">*pViewTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc6a5-107">*pViewTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc6a5-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc6a5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bc6a5-109">Puntero a un D3DXMATRIX que contiene una transformación del objeto Sprite del espacio universal original.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-109">Pointer to a D3DXMATRIX that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="bc6a5-110">Use esta transformación para escalar, girar o transformar el sprite.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc6a5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc6a5-111">Return value</span></span>

<span data-ttu-id="bc6a5-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc6a5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc6a5-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc6a5-114">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bc6a5-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6a5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc6a5-115">Requirements</span></span>



| <span data-ttu-id="bc6a5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc6a5-116">Requirement</span></span> | <span data-ttu-id="bc6a5-117">Value</span><span class="sxs-lookup"><span data-stu-id="bc6a5-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6a5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc6a5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bc6a5-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc6a5-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc6a5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc6a5-120">Library</span></span><br/> | <dl> <span data-ttu-id="bc6a5-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc6a5-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc6a5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc6a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6a5-123">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="bc6a5-123">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="bc6a5-124">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bc6a5-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
