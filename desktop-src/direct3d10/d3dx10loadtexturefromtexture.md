---
description: Cargar una textura de una textura.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Función D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362486"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="1fc7f-103">D3DX10LoadTextureFromTexture función)</span><span class="sxs-lookup"><span data-stu-id="1fc7f-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="1fc7f-104">Cargar una textura de una textura.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fc7f-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="1fc7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fc7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc7f-107">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="1fc7f-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc7f-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="1fc7f-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="1fc7f-109">Puntero a la textura de origen.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-109">Pointer to the source texture.</span></span> <span data-ttu-id="1fc7f-110">Vea [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="1fc7f-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="1fc7f-111">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="1fc7f-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc7f-112">Tipo: **[ **D3DX10 \_ \_ \_ información de carga de textura**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fc7f-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="1fc7f-113">Puntero a los parámetros de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="1fc7f-114">Consulte [**información sobre la carga de textura de D3DX10 \_ \_ \_**](d3dx10-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="1fc7f-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fc7f-115">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="1fc7f-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc7f-116">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="1fc7f-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="1fc7f-117">Puntero a la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="1fc7f-117">Pointer to the destination texture.</span></span> <span data-ttu-id="1fc7f-118">Consulte la [**interfaz ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="1fc7f-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc7f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fc7f-119">Return value</span></span>

<span data-ttu-id="1fc7f-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fc7f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fc7f-121">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1fc7f-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc7f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc7f-122">Requirements</span></span>



| <span data-ttu-id="1fc7f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc7f-123">Requirement</span></span> | <span data-ttu-id="1fc7f-124">Value</span><span class="sxs-lookup"><span data-stu-id="1fc7f-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc7f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fc7f-125">Header</span></span><br/> | <dl> <span data-ttu-id="1fc7f-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc7f-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc7f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fc7f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc7f-128">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="1fc7f-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




