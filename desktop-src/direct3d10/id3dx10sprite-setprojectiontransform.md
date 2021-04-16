---
description: Establezca la matriz de proyección para todos los sprites.
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: 'ID3DX10Sprite:: SetProjectionTransform (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c49fb570f87c8c86313e1f4adcf1560fee909433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548142"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a><span data-ttu-id="4429c-103">ID3DX10Sprite:: SetProjectionTransform (método)</span><span class="sxs-lookup"><span data-stu-id="4429c-103">ID3DX10Sprite::SetProjectionTransform method</span></span>

<span data-ttu-id="4429c-104">Establezca la matriz de proyección para todos los sprites.</span><span class="sxs-lookup"><span data-stu-id="4429c-104">Set the projection matrix for all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="4429c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4429c-105">Syntax</span></span>


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="4429c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4429c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4429c-107">*pProjectionTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4429c-107">*pProjectionTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4429c-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4429c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4429c-109">Matriz de proyección que se va a usar en todos los sprites.</span><span class="sxs-lookup"><span data-stu-id="4429c-109">The projection matrix to be used on all sprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4429c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4429c-110">Return value</span></span>

<span data-ttu-id="4429c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4429c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4429c-112">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4429c-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4429c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4429c-113">Requirements</span></span>



| <span data-ttu-id="4429c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4429c-114">Requirement</span></span> | <span data-ttu-id="4429c-115">Value</span><span class="sxs-lookup"><span data-stu-id="4429c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4429c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4429c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4429c-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4429c-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4429c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4429c-118">Library</span></span><br/> | <dl> <span data-ttu-id="4429c-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4429c-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4429c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4429c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4429c-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="4429c-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="4429c-122">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="4429c-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
