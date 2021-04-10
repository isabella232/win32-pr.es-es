---
description: Obtiene la transformación de Sprite.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'ID3DXSprite:: GetTransform (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083746"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="9c388-103">ID3DXSprite:: GetTransform (método)</span><span class="sxs-lookup"><span data-stu-id="9c388-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="9c388-104">Obtiene la transformación de Sprite.</span><span class="sxs-lookup"><span data-stu-id="9c388-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c388-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c388-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="9c388-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c388-107">*pTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c388-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c388-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c388-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9c388-109">Puntero a un [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación del objeto Sprite del espacio universal original.</span><span class="sxs-lookup"><span data-stu-id="9c388-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c388-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c388-110">Return value</span></span>

<span data-ttu-id="9c388-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c388-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c388-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c388-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9c388-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="9c388-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="9c388-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c388-114">Requirements</span></span>



| <span data-ttu-id="9c388-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c388-115">Requirement</span></span> | <span data-ttu-id="9c388-116">Value</span><span class="sxs-lookup"><span data-stu-id="9c388-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c388-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c388-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9c388-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c388-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9c388-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c388-119">Library</span></span><br/> | <dl> <span data-ttu-id="9c388-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c388-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c388-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c388-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c388-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="9c388-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




