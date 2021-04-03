---
description: Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: ID3DXFont::P método reloadGlyphs (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083802"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="ceb8c-103">ID3DXFont::P método reloadGlyphs</span><span class="sxs-lookup"><span data-stu-id="ceb8c-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="ceb8c-104">Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ceb8c-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="ceb8c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ceb8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb8c-107">*Primero* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ceb8c-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb8c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceb8c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceb8c-109">IDENTIFICADOR del primer glifo que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="ceb8c-110">*Última* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ceb8c-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb8c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceb8c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceb8c-112">IDENTIFICADOR del último glifo que se va a cargar en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb8c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ceb8c-113">Return value</span></span>

<span data-ttu-id="ceb8c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ceb8c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ceb8c-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ceb8c-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb8c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ceb8c-117">Remarks</span></span>

<span data-ttu-id="ceb8c-118">Este método genera texturas que contienen los glifos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="ceb8c-119">Los glifos se dibujan como una serie de triángulos.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="ceb8c-120">Los glifos no se representarán en el dispositivo; También se debe llamar a [**DrawText**](id3dxfont--drawtext.md) para representar los glifos.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="ceb8c-121">Sin embargo, al precargar los glifos en la memoria de vídeo, **DrawText** usará prácticamente menos recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="ceb8c-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb8c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceb8c-122">Requirements</span></span>



| <span data-ttu-id="ceb8c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceb8c-123">Requirement</span></span> | <span data-ttu-id="ceb8c-124">Value</span><span class="sxs-lookup"><span data-stu-id="ceb8c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb8c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ceb8c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ceb8c-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceb8c-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ceb8c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ceb8c-127">Library</span></span><br/> | <dl> <span data-ttu-id="ceb8c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ceb8c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ceb8c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ceb8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb8c-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="ceb8c-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
