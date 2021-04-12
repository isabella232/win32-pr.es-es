---
description: Crea un objeto Font. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar DirectWrite y la biblioteca DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Función D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362496"
---
# <a name="d3dx10createfontindirect-function"></a><span data-ttu-id="c49bc-103">D3DX10CreateFontIndirect función)</span><span class="sxs-lookup"><span data-stu-id="c49bc-103">D3DX10CreateFontIndirect function</span></span>

<span data-ttu-id="c49bc-104">Crea un objeto Font.</span><span class="sxs-lookup"><span data-stu-id="c49bc-104">Creates a font object.</span></span>

> [!Note]  
> <span data-ttu-id="c49bc-105">En lugar de usar esta función, se recomienda usar [DirectWrite](../directwrite/direct-write-portal.md) y la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.</span><span class="sxs-lookup"><span data-stu-id="c49bc-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c49bc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c49bc-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="c49bc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c49bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c49bc-108">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c49bc-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49bc-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c49bc-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c49bc-110">Puntero a una interfaz de [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="c49bc-110">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c49bc-111">*pDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c49bc-111">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49bc-112">Tipo: **const [**D3DX10 \_ \_ Descripción**](d3dx10-font-desc.md) \*** de la fuente</span><span class="sxs-lookup"><span data-stu-id="c49bc-112">Type: **const [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="c49bc-113">Puntero a una estructura de [**\_ \_ DESC de fuente D3DX10**](d3dx10-font-desc.md) , que describe los atributos del objeto de fuente que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c49bc-113">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="c49bc-114">Si se define Unicode, la llamada de función se resuelve como D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="c49bc-114">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="c49bc-115">De lo contrario, la llamada de función se resuelve como D3DXCreateFontIndirectA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="c49bc-115">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

</dd> <dt>

<span data-ttu-id="c49bc-116">*ppFont* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c49bc-116">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c49bc-117">Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="c49bc-117">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="c49bc-118">Devuelve un puntero a una [**interfaz ID3DX10Font**](id3dx10font.md).</span><span class="sxs-lookup"><span data-stu-id="c49bc-118">Returns a pointer to an [**ID3DX10Font Interface**](id3dx10font.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c49bc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c49bc-119">Return value</span></span>

<span data-ttu-id="c49bc-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c49bc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c49bc-121">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c49bc-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c49bc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c49bc-122">Requirements</span></span>



| <span data-ttu-id="c49bc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c49bc-123">Requirement</span></span> | <span data-ttu-id="c49bc-124">Value</span><span class="sxs-lookup"><span data-stu-id="c49bc-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c49bc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c49bc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c49bc-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c49bc-126"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="c49bc-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c49bc-127">Library</span></span><br/> | <dl> <span data-ttu-id="c49bc-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c49bc-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c49bc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c49bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49bc-130">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="c49bc-130">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
