---
description: Inicie la representación de un mapa de entorno de Hemispheric.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'ID3DXRenderToEnvMap:: BeginHemisphere (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280291"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="62a4d-103">ID3DXRenderToEnvMap:: BeginHemisphere (método)</span><span class="sxs-lookup"><span data-stu-id="62a4d-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="62a4d-104">Inicie la representación de un mapa de entorno de Hemispheric.</span><span class="sxs-lookup"><span data-stu-id="62a4d-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62a4d-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="62a4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a4d-107">*pTexZPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a4d-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a4d-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="62a4d-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="62a4d-109">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la superficie de representación de textura positiva.</span><span class="sxs-lookup"><span data-stu-id="62a4d-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="62a4d-110">*pTexZNeg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62a4d-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a4d-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="62a4d-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="62a4d-112">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la superficie de representación de textura negativa.</span><span class="sxs-lookup"><span data-stu-id="62a4d-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a4d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62a4d-113">Return value</span></span>

<span data-ttu-id="62a4d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62a4d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62a4d-115">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62a4d-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62a4d-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL. E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="62a4d-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="62a4d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62a4d-117">Remarks</span></span>

<span data-ttu-id="62a4d-118">Vea [**ID3DXRenderToEnvMap:: facial**](id3dxrendertoenvmap--face.md) para dibujar la superficie.</span><span class="sxs-lookup"><span data-stu-id="62a4d-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a4d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a4d-119">Requirements</span></span>



| <span data-ttu-id="62a4d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a4d-120">Requirement</span></span> | <span data-ttu-id="62a4d-121">Value</span><span class="sxs-lookup"><span data-stu-id="62a4d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62a4d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62a4d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="62a4d-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="62a4d-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="62a4d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62a4d-124">Library</span></span><br/> | <dl> <span data-ttu-id="62a4d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a4d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62a4d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a4d-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="62a4d-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="62a4d-128">**ID3DXRenderToEnvMap:: end**</span><span class="sxs-lookup"><span data-stu-id="62a4d-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
