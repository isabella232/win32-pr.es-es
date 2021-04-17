---
description: Establece una textura.
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'ID3DXBaseEffect:: SetTexture (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721425"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="5b7f0-103">ID3DXBaseEffect:: SetTexture (método)</span><span class="sxs-lookup"><span data-stu-id="5b7f0-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="5b7f0-104">Establece una textura.</span><span class="sxs-lookup"><span data-stu-id="5b7f0-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b7f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b7f0-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="5b7f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b7f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b7f0-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b7f0-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b7f0-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5b7f0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5b7f0-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="5b7f0-109">Unique identifier.</span></span> <span data-ttu-id="5b7f0-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5b7f0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b7f0-111">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b7f0-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b7f0-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="5b7f0-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="5b7f0-113">Objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="5b7f0-113">Texture object.</span></span> <span data-ttu-id="5b7f0-114">Vea [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="5b7f0-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b7f0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b7f0-115">Return value</span></span>

<span data-ttu-id="5b7f0-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b7f0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b7f0-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b7f0-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b7f0-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5b7f0-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b7f0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b7f0-119">Requirements</span></span>



| <span data-ttu-id="5b7f0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b7f0-120">Requirement</span></span> | <span data-ttu-id="5b7f0-121">Value</span><span class="sxs-lookup"><span data-stu-id="5b7f0-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7f0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b7f0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5b7f0-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b7f0-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5b7f0-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b7f0-124">Library</span></span><br/> | <dl> <span data-ttu-id="5b7f0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b7f0-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5b7f0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b7f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7f0-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5b7f0-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5b7f0-128">**GetTexture**</span><span class="sxs-lookup"><span data-stu-id="5b7f0-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
