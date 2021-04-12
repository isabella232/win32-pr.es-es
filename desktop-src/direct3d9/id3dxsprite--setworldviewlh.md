---
description: Establece la transformación de vista universal que se entrega a la izquierda de un objeto Sprite. Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'ID3DXSprite:: SetWorldViewLH (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280382"
---
# <a name="id3dxspritesetworldviewlh-method"></a><span data-ttu-id="6d64c-104">ID3DXSprite:: SetWorldViewLH (método)</span><span class="sxs-lookup"><span data-stu-id="6d64c-104">ID3DXSprite::SetWorldViewLH method</span></span>

<span data-ttu-id="6d64c-105">Establece la transformación de vista universal que se entrega a la izquierda de un objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="6d64c-105">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="6d64c-106">Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.</span><span class="sxs-lookup"><span data-stu-id="6d64c-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d64c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d64c-107">Syntax</span></span>


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="6d64c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d64c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d64c-109">*pWorld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d64c-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d64c-110">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d64c-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d64c-111">Puntero a un [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación universal.</span><span class="sxs-lookup"><span data-stu-id="6d64c-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="6d64c-112">Si es **null**, se utiliza la matriz de identidad para la transformación del mundo.</span><span class="sxs-lookup"><span data-stu-id="6d64c-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="6d64c-113">*pView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d64c-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d64c-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d64c-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6d64c-115">Puntero a un [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación de vista.</span><span class="sxs-lookup"><span data-stu-id="6d64c-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="6d64c-116">Si es **null**, se utiliza la matriz de identidad para la transformación de la vista.</span><span class="sxs-lookup"><span data-stu-id="6d64c-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d64c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d64c-117">Return value</span></span>

<span data-ttu-id="6d64c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d64c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d64c-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d64c-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6d64c-120">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6d64c-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6d64c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d64c-121">Remarks</span></span>

<span data-ttu-id="6d64c-122">Se requiere una llamada a este método (o a [**ID3DXSprite:: SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) si el objeto Sprite se va a representar con el valor de marca D3DXSprite de la [ \_ \_ cartelera](d3dxsprite.md), D3DXSprite de \_ \_ profundidad de orden \_ \_ FRONTTOBACK o D3DXSprite \_ \_ \_ de profundidad de ordenación BACKTOFRONT \_ en [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="6d64c-122">A call to this method (or to [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d64c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d64c-123">Requirements</span></span>



| <span data-ttu-id="6d64c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d64c-124">Requirement</span></span> | <span data-ttu-id="6d64c-125">Value</span><span class="sxs-lookup"><span data-stu-id="6d64c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d64c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d64c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6d64c-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d64c-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6d64c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d64c-128">Library</span></span><br/> | <dl> <span data-ttu-id="6d64c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d64c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6d64c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d64c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d64c-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="6d64c-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




