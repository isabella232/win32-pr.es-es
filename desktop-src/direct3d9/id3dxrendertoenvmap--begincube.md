---
description: Inicie la representación de un mapa de entorno cúbico.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'ID3DXRenderToEnvMap:: BeginCube (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362514"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a><span data-ttu-id="8cba7-103">ID3DXRenderToEnvMap:: BeginCube (método)</span><span class="sxs-lookup"><span data-stu-id="8cba7-103">ID3DXRenderToEnvMap::BeginCube method</span></span>

<span data-ttu-id="8cba7-104">Inicie la representación de un mapa de entorno cúbico.</span><span class="sxs-lookup"><span data-stu-id="8cba7-104">Initiate the rendering of a cubic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cba7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cba7-105">Syntax</span></span>


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a><span data-ttu-id="8cba7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cba7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cba7-107">*pCubeTex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cba7-107">*pCubeTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cba7-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="8cba7-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="8cba7-109">Puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa la textura del cubo en la que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="8cba7-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface that represents the cube texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cba7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cba7-110">Return value</span></span>

<span data-ttu-id="8cba7-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cba7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cba7-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8cba7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8cba7-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8cba7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cba7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cba7-114">Remarks</span></span>

<span data-ttu-id="8cba7-115">Vea [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) para dibujar cada una de las 6 caras.</span><span class="sxs-lookup"><span data-stu-id="8cba7-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw each of the 6 faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cba7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cba7-116">Requirements</span></span>



| <span data-ttu-id="8cba7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cba7-117">Requirement</span></span> | <span data-ttu-id="8cba7-118">Value</span><span class="sxs-lookup"><span data-stu-id="8cba7-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cba7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cba7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8cba7-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cba7-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8cba7-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cba7-121">Library</span></span><br/> | <dl> <span data-ttu-id="8cba7-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cba7-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cba7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cba7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cba7-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="8cba7-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="8cba7-125">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="8cba7-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
