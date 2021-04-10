---
description: La interfaz ID3DX10Font encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interfaz ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280340"
---
# <a name="id3dx10font-interface"></a><span data-ttu-id="7b4a0-103">Interfaz ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="7b4a0-103">ID3DX10Font interface</span></span>

<span data-ttu-id="7b4a0-104">La interfaz ID3DX10Font encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-104">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="7b4a0-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b4a0-105">Members</span></span>

<span data-ttu-id="7b4a0-106">La interfaz **ID3DX10Font** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7b4a0-106">The **ID3DX10Font** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7b4a0-107">**ID3DX10Font** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7b4a0-107">**ID3DX10Font** also has these types of members:</span></span>

-   [<span data-ttu-id="7b4a0-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b4a0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7b4a0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b4a0-109">Methods</span></span>

<span data-ttu-id="7b4a0-110">La interfaz **ID3DX10Font** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-110">The **ID3DX10Font** interface has these methods.</span></span>



| <span data-ttu-id="7b4a0-111">Método</span><span class="sxs-lookup"><span data-stu-id="7b4a0-111">Method</span></span>                                                     | <span data-ttu-id="7b4a0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b4a0-112">Description</span></span>                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b4a0-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-113">**DrawText**</span></span>](id3dx10font-drawtext.md)                   | <span data-ttu-id="7b4a0-114">Dibujar texto con formato.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-114">Draw formatted text.</span></span> <span data-ttu-id="7b4a0-115">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                        |
| [<span data-ttu-id="7b4a0-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-116">**GetDC**</span></span>](id3dx10font-getdc.md)                         | <span data-ttu-id="7b4a0-117">Devuelve un identificador a un contexto de dispositivo de pantalla (DC) que tiene la fuente establecida en él.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-117">Return a handle to a display device context (DC) that has the font set onto it.</span></span><br/>                                                            |
| [<span data-ttu-id="7b4a0-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-118">**GetDesc**</span></span>](id3dx10font-getdesc.md)                     | <span data-ttu-id="7b4a0-119">Obtiene una descripción del objeto de fuente actual.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-119">Get a description of the current font object.</span></span><br/>                                                                                              |
| [<span data-ttu-id="7b4a0-120">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-120">**GetDevice**</span></span>](id3dx10font-getdevice.md)                 | <span data-ttu-id="7b4a0-121">Recupere el dispositivo Direct3D asociado al objeto Font.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-121">Retrieve the Direct3D device associated with the font object.</span></span><br/>                                                                              |
| [<span data-ttu-id="7b4a0-122">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-122">**GetGlyphData**</span></span>](id3dx10font-getglyphdata.md)           | <span data-ttu-id="7b4a0-123">Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-123">Return information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                     |
| [<span data-ttu-id="7b4a0-124">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-124">**GetTextMetrics**</span></span>](id3dx10font-gettextmetrics.md)       | <span data-ttu-id="7b4a0-125">Recupera las características de la fuente.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-125">Retrieve font characteristics.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="7b4a0-126">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-126">**PreloadCharacters**</span></span>](id3dx10font-preloadcharacters.md) | <span data-ttu-id="7b4a0-127">Cargar una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-127">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                        |
| [<span data-ttu-id="7b4a0-128">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-128">**PreloadGlyphs**</span></span>](id3dx10font-preloadglyphs.md)         | <span data-ttu-id="7b4a0-129">Cargue una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-129">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                            |
| [<span data-ttu-id="7b4a0-130">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="7b4a0-130">**PreloadText**</span></span>](id3dx10font-preloadtext.md)             | <span data-ttu-id="7b4a0-131">Cargue texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-131">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="7b4a0-132">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-132">This method supports ANSI and Unicode strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b4a0-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b4a0-133">Remarks</span></span>

<span data-ttu-id="7b4a0-134">La interfaz ID3DX10Font se obtiene llamando a [**D3DX10CreateFont**](d3dx10createfont.md) o [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="7b4a0-134">The ID3DX10Font interface is obtained by calling [**D3DX10CreateFont**](d3dx10createfont.md) or [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).</span></span>

<span data-ttu-id="7b4a0-135">El tipo LPD3DX10FONT se define como un puntero a la interfaz ID3DX10Font.</span><span class="sxs-lookup"><span data-stu-id="7b4a0-135">The LPD3DX10FONT type is defined as a pointer to the ID3DX10Font interface.</span></span>


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a><span data-ttu-id="7b4a0-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b4a0-136">Requirements</span></span>



| <span data-ttu-id="7b4a0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b4a0-137">Requirement</span></span> | <span data-ttu-id="7b4a0-138">Value</span><span class="sxs-lookup"><span data-stu-id="7b4a0-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4a0-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b4a0-139">Header</span></span><br/>  | <dl> <span data-ttu-id="7b4a0-140"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a0-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b4a0-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b4a0-141">Library</span></span><br/> | <dl> <span data-ttu-id="7b4a0-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a0-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4a0-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b4a0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4a0-144">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="7b4a0-144">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
