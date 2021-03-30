---
description: Establece la transformación de Sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'ID3DXSprite:: SetTransform (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280383"
---
# <a name="id3dxspritesettransform-method"></a><span data-ttu-id="d461f-103">ID3DXSprite:: SetTransform (método)</span><span class="sxs-lookup"><span data-stu-id="d461f-103">ID3DXSprite::SetTransform method</span></span>

<span data-ttu-id="d461f-104">Establece la transformación de Sprite.</span><span class="sxs-lookup"><span data-stu-id="d461f-104">Sets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="d461f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d461f-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="d461f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d461f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d461f-107">*pTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d461f-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d461f-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d461f-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d461f-109">Puntero a un [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación del objeto Sprite del espacio universal original.</span><span class="sxs-lookup"><span data-stu-id="d461f-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="d461f-110">Use esta transformación para escalar, girar o transformar el sprite.</span><span class="sxs-lookup"><span data-stu-id="d461f-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d461f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d461f-111">Return value</span></span>

<span data-ttu-id="d461f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d461f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d461f-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d461f-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d461f-114">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d461f-114">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="d461f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d461f-115">Requirements</span></span>



| <span data-ttu-id="d461f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d461f-116">Requirement</span></span> | <span data-ttu-id="d461f-117">Value</span><span class="sxs-lookup"><span data-stu-id="d461f-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d461f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d461f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d461f-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d461f-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d461f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d461f-120">Library</span></span><br/> | <dl> <span data-ttu-id="d461f-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d461f-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d461f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d461f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d461f-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="d461f-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="d461f-124">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d461f-124">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




