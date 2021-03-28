---
title: Función D3DX11LoadTextureFromTexture (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, cambiar el tamaño, convertir, comprimir, descomprimir o CopyRectangle. Cargar una textura de una textura.
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- Función D3DX11LoadTextureFromTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986995"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="64a7f-106">D3DX11LoadTextureFromTexture función)</span><span class="sxs-lookup"><span data-stu-id="64a7f-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="64a7f-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="64a7f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="64a7f-108">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , cambiar el **tamaño**, **convertir**, **comprimir**, **descomprimir** o **CopyRectangle**.</span><span class="sxs-lookup"><span data-stu-id="64a7f-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="64a7f-109">Cargar una textura de una textura.</span><span class="sxs-lookup"><span data-stu-id="64a7f-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a7f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64a7f-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="64a7f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64a7f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a7f-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="64a7f-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="64a7f-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="64a7f-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="64a7f-114">Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="64a7f-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="64a7f-115">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="64a7f-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="64a7f-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="64a7f-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="64a7f-117">Puntero a la textura de origen.</span><span class="sxs-lookup"><span data-stu-id="64a7f-117">Pointer to the source texture.</span></span> <span data-ttu-id="64a7f-118">Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="64a7f-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="64a7f-119">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="64a7f-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="64a7f-120">Tipo: **[ **D3DX11 \_ \_ \_ información de carga de textura**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="64a7f-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="64a7f-121">Puntero a los parámetros de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="64a7f-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="64a7f-122">Consulte [**información sobre la carga de textura de D3DX11 \_ \_ \_**](d3dx11-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="64a7f-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="64a7f-123">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="64a7f-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="64a7f-124">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="64a7f-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="64a7f-125">Puntero a la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="64a7f-125">Pointer to the destination texture.</span></span> <span data-ttu-id="64a7f-126">Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="64a7f-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64a7f-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64a7f-127">Return value</span></span>

<span data-ttu-id="64a7f-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64a7f-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64a7f-129">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="64a7f-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64a7f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64a7f-130">Requirements</span></span>



| <span data-ttu-id="64a7f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="64a7f-131">Requirement</span></span> | <span data-ttu-id="64a7f-132">Value</span><span class="sxs-lookup"><span data-stu-id="64a7f-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64a7f-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64a7f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="64a7f-134"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="64a7f-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="64a7f-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64a7f-135">Library</span></span><br/> | <dl> <span data-ttu-id="64a7f-136"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64a7f-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="64a7f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="64a7f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a7f-138">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="64a7f-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





