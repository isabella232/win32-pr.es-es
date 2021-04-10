---
description: Inicie la representación de un mapa de entorno de parabólica.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'ID3DXRenderToEnvMap:: BeginParabolic (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083714"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a><span data-ttu-id="98b54-103">ID3DXRenderToEnvMap:: BeginParabolic (método)</span><span class="sxs-lookup"><span data-stu-id="98b54-103">ID3DXRenderToEnvMap::BeginParabolic method</span></span>

<span data-ttu-id="98b54-104">Inicie la representación de un mapa de entorno de parabólica.</span><span class="sxs-lookup"><span data-stu-id="98b54-104">Initiate the rendering of a parabolic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98b54-105">Syntax</span></span>


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="98b54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98b54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98b54-107">*pTexZPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98b54-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98b54-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="98b54-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="98b54-109">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de representación positiva.</span><span class="sxs-lookup"><span data-stu-id="98b54-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive render texture.</span></span>

</dd> <dt>

<span data-ttu-id="98b54-110">*pTexZNeg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98b54-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98b54-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="98b54-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="98b54-112">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de representación negativa.</span><span class="sxs-lookup"><span data-stu-id="98b54-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative render texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98b54-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98b54-113">Return value</span></span>

<span data-ttu-id="98b54-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98b54-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98b54-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="98b54-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="98b54-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL. E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="98b54-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="98b54-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98b54-117">Remarks</span></span>

<span data-ttu-id="98b54-118">Vea [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) para dibujar las caras.</span><span class="sxs-lookup"><span data-stu-id="98b54-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b54-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98b54-119">Requirements</span></span>



| <span data-ttu-id="98b54-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98b54-120">Requirement</span></span> | <span data-ttu-id="98b54-121">Value</span><span class="sxs-lookup"><span data-stu-id="98b54-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98b54-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98b54-122">Header</span></span><br/>  | <dl> <span data-ttu-id="98b54-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="98b54-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="98b54-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98b54-124">Library</span></span><br/> | <dl> <span data-ttu-id="98b54-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98b54-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98b54-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="98b54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b54-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="98b54-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="98b54-128">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="98b54-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
