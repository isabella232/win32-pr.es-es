---
description: Inicie la representación de un mapa de entorno esférico.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap:: BeginSphere (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362513"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="f61a6-103">ID3DXRenderToEnvMap:: BeginSphere (método)</span><span class="sxs-lookup"><span data-stu-id="f61a6-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="f61a6-104">Inicie la representación de un mapa de entorno esférico.</span><span class="sxs-lookup"><span data-stu-id="f61a6-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f61a6-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="f61a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f61a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61a6-107">*pTex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f61a6-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61a6-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f61a6-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f61a6-109">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura a la que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="f61a6-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61a6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f61a6-110">Return value</span></span>

<span data-ttu-id="f61a6-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f61a6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f61a6-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f61a6-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f61a6-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL. E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="f61a6-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="f61a6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f61a6-114">Remarks</span></span>

<span data-ttu-id="f61a6-115">Vea [**ID3DXRenderToEnvMap:: facial**](id3dxrendertoenvmap--face.md) para dibujar la superficie.</span><span class="sxs-lookup"><span data-stu-id="f61a6-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61a6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f61a6-116">Requirements</span></span>



| <span data-ttu-id="f61a6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61a6-117">Requirement</span></span> | <span data-ttu-id="f61a6-118">Value</span><span class="sxs-lookup"><span data-stu-id="f61a6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f61a6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f61a6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f61a6-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61a6-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f61a6-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f61a6-121">Library</span></span><br/> | <dl> <span data-ttu-id="f61a6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f61a6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f61a6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f61a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61a6-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="f61a6-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="f61a6-125">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="f61a6-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
