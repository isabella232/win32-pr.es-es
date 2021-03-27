---
title: Función D3DX11FilterTexture (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, GenerateMipMaps y GenerateMipMaps3D. Genera una cadena de mipmap mediante un filtro de textura determinado.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- Función D3DX11FilterTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987007"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="24a59-106">D3DX11FilterTexture función)</span><span class="sxs-lookup"><span data-stu-id="24a59-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="24a59-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="24a59-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="24a59-108">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GenerateMipMaps** y **GenerateMipMaps3D**.</span><span class="sxs-lookup"><span data-stu-id="24a59-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="24a59-109">Genera una cadena de mipmap mediante un filtro de textura determinado.</span><span class="sxs-lookup"><span data-stu-id="24a59-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a59-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24a59-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="24a59-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24a59-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a59-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="24a59-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="24a59-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="24a59-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="24a59-114">Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="24a59-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="24a59-115">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="24a59-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="24a59-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="24a59-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="24a59-117">Objeto de textura que se va a filtrar.</span><span class="sxs-lookup"><span data-stu-id="24a59-117">The texture object to be filtered.</span></span> <span data-ttu-id="24a59-118">Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="24a59-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="24a59-119">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="24a59-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="24a59-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24a59-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24a59-121">Nivel de mipmap cuyos datos se utilizan para generar el resto de la cadena de mipmap.</span><span class="sxs-lookup"><span data-stu-id="24a59-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="24a59-122">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="24a59-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="24a59-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24a59-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24a59-124">Marcas que controlan la forma en que se filtra cada miplevel (o el \_ valor predeterminado de D3DX11 para el \_ filtro \_ lineal D3DX11).</span><span class="sxs-lookup"><span data-stu-id="24a59-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="24a59-125">Vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="24a59-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a59-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24a59-126">Return value</span></span>

<span data-ttu-id="24a59-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24a59-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24a59-128">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="24a59-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24a59-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24a59-129">Requirements</span></span>



| <span data-ttu-id="24a59-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a59-130">Requirement</span></span> | <span data-ttu-id="24a59-131">Value</span><span class="sxs-lookup"><span data-stu-id="24a59-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a59-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24a59-132">Header</span></span><br/>  | <dl> <span data-ttu-id="24a59-133"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a59-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="24a59-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24a59-134">Library</span></span><br/> | <dl> <span data-ttu-id="24a59-135"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24a59-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="24a59-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="24a59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a59-137">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="24a59-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

