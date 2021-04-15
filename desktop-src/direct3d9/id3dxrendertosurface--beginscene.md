---
description: Comienza una escena.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface:: BeginScene (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649451"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a><span data-ttu-id="c72a4-103">ID3DXRenderToSurface:: BeginScene (método)</span><span class="sxs-lookup"><span data-stu-id="c72a4-103">ID3DXRenderToSurface::BeginScene method</span></span>

<span data-ttu-id="c72a4-104">Comienza una escena.</span><span class="sxs-lookup"><span data-stu-id="c72a4-104">Begins a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="c72a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c72a4-105">Syntax</span></span>


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a><span data-ttu-id="c72a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c72a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c72a4-107">*pSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c72a4-107">*pSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c72a4-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="c72a4-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="c72a4-109">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que representa la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="c72a4-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="c72a4-110">*pViewport* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c72a4-110">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c72a4-111">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="c72a4-111">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="c72a4-112">Puntero a una estructura [**D3DVIEWPORT9**](d3dviewport9.md) , que describe la ventanilla de la escena.</span><span class="sxs-lookup"><span data-stu-id="c72a4-112">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c72a4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c72a4-113">Return value</span></span>

<span data-ttu-id="c72a4-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c72a4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c72a4-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c72a4-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c72a4-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c72a4-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY</span></span>

## <a name="requirements"></a><span data-ttu-id="c72a4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c72a4-117">Requirements</span></span>



| <span data-ttu-id="c72a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c72a4-118">Requirement</span></span> | <span data-ttu-id="c72a4-119">Value</span><span class="sxs-lookup"><span data-stu-id="c72a4-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c72a4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c72a4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c72a4-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c72a4-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c72a4-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c72a4-122">Library</span></span><br/> | <dl> <span data-ttu-id="c72a4-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c72a4-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c72a4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c72a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72a4-125">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="c72a4-125">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="c72a4-126">**ID3DXRenderToSurface::EndScene**</span><span class="sxs-lookup"><span data-stu-id="c72a4-126">**ID3DXRenderToSurface::EndScene**</span></span>](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
