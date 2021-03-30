---
description: Agrega un marco secundario a un marco.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: Función D3DXFrameAppendChild (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280319"
---
# <a name="d3dxframeappendchild-function"></a><span data-ttu-id="30816-103">D3DXFrameAppendChild función)</span><span class="sxs-lookup"><span data-stu-id="30816-103">D3DXFrameAppendChild function</span></span>

<span data-ttu-id="30816-104">Agrega un marco secundario a un marco.</span><span class="sxs-lookup"><span data-stu-id="30816-104">Adds a child frame to a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="30816-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30816-105">Syntax</span></span>


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a><span data-ttu-id="30816-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30816-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30816-107">*pFrameParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30816-107">*pFrameParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30816-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="30816-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="30816-109">Puntero al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="30816-109">Pointer to the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="30816-110">*pFrameChild* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30816-110">*pFrameChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30816-111">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="30816-111">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="30816-112">Puntero al nodo secundario.</span><span class="sxs-lookup"><span data-stu-id="30816-112">Pointer to the child node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30816-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30816-113">Return value</span></span>

<span data-ttu-id="30816-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30816-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30816-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30816-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30816-116">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="30816-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="30816-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30816-117">Requirements</span></span>



| <span data-ttu-id="30816-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30816-118">Requirement</span></span> | <span data-ttu-id="30816-119">Value</span><span class="sxs-lookup"><span data-stu-id="30816-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30816-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30816-120">Header</span></span><br/>  | <dl> <span data-ttu-id="30816-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="30816-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="30816-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30816-122">Library</span></span><br/> | <dl> <span data-ttu-id="30816-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30816-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30816-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="30816-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30816-125">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="30816-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




