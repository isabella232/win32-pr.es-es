---
description: La interfaz ID3DXFont encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interfaz ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b3919e4198feddbe4ac193f58f63d48753aa94d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698396"
---
# <a name="id3dxfont-interface"></a><span data-ttu-id="70b14-103">Interfaz ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="70b14-103">ID3DXFont interface</span></span>

<span data-ttu-id="70b14-104">La interfaz ID3DXFont encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="70b14-104">The ID3DXFont interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span>

## <a name="members"></a><span data-ttu-id="70b14-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="70b14-105">Members</span></span>

<span data-ttu-id="70b14-106">La interfaz **ID3DXFont** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="70b14-106">The **ID3DXFont** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="70b14-107">**ID3DXFont** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="70b14-107">**ID3DXFont** also has these types of members:</span></span>

-   [<span data-ttu-id="70b14-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="70b14-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70b14-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="70b14-109">Methods</span></span>

<span data-ttu-id="70b14-110">La interfaz **ID3DXFont** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="70b14-110">The **ID3DXFont** interface has these methods.</span></span>



| <span data-ttu-id="70b14-111">Método</span><span class="sxs-lookup"><span data-stu-id="70b14-111">Method</span></span>                                                    | <span data-ttu-id="70b14-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="70b14-112">Description</span></span>                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70b14-113">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="70b14-113">**DrawText**</span></span>](id3dxfont--drawtext.md)                   | <span data-ttu-id="70b14-114">Dibuja texto con formato.</span><span class="sxs-lookup"><span data-stu-id="70b14-114">Draws formatted text.</span></span> <span data-ttu-id="70b14-115">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="70b14-115">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="70b14-116">**GetDC**</span><span class="sxs-lookup"><span data-stu-id="70b14-116">**GetDC**</span></span>](id3dxfont--getdc.md)                         | <span data-ttu-id="70b14-117">Devuelve un identificador para un contexto de dispositivo de pantalla (DC) que tiene el conjunto de fuentes.</span><span class="sxs-lookup"><span data-stu-id="70b14-117">Returns a handle to a display device context (DC) that has the font set.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="70b14-118">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="70b14-118">**GetDesc**</span></span>](id3dxfont--getdesc.md)                     | <span data-ttu-id="70b14-119">Obtiene una descripción del objeto de fuente actual.</span><span class="sxs-lookup"><span data-stu-id="70b14-119">Gets a description of the current font object.</span></span> <span data-ttu-id="70b14-120">GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una estructura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="70b14-120">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span><br/> |
| [<span data-ttu-id="70b14-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="70b14-121">**GetDevice**</span></span>](id3dxfont--getdevice.md)                 | <span data-ttu-id="70b14-122">Recupera el dispositivo Direct3D asociado al objeto Font.</span><span class="sxs-lookup"><span data-stu-id="70b14-122">Retrieves the Direct3D device associated with the font object.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="70b14-123">**GetGlyphData**</span><span class="sxs-lookup"><span data-stu-id="70b14-123">**GetGlyphData**</span></span>](id3dxfont--getglyphdata.md)           | <span data-ttu-id="70b14-124">Devuelve información sobre la posición y la orientación de un glifo en una celda de carácter.</span><span class="sxs-lookup"><span data-stu-id="70b14-124">Returns information about the placement and orientation of a glyph in a character cell.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="70b14-125">**GetTextMetrics**</span><span class="sxs-lookup"><span data-stu-id="70b14-125">**GetTextMetrics**</span></span>](id3dxfont--gettextmetrics.md)       | <span data-ttu-id="70b14-126">Recupera las características de fuente que se identifican en una estructura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="70b14-126">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="70b14-127">Este método admite la configuración del compilador ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="70b14-127">This method supports ANSI and Unicode compiler settings.</span></span><br/>                                                                       |
| [<span data-ttu-id="70b14-128">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="70b14-128">**OnLostDevice**</span></span>](id3dxfont--onlostdevice.md)           | <span data-ttu-id="70b14-129">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="70b14-129">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="70b14-130">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70b14-130">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/>                                              |
| [<span data-ttu-id="70b14-131">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="70b14-131">**OnResetDevice**</span></span>](id3dxfont--onresetdevice.md)         | <span data-ttu-id="70b14-132">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="70b14-132">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="70b14-133">**PreloadCharacters**</span><span class="sxs-lookup"><span data-stu-id="70b14-133">**PreloadCharacters**</span></span>](id3dxfont--preloadcharacters.md) | <span data-ttu-id="70b14-134">Carga una serie de caracteres en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70b14-134">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="70b14-135">**PreloadGlyphs**</span><span class="sxs-lookup"><span data-stu-id="70b14-135">**PreloadGlyphs**</span></span>](id3dxfont--preloadglyphs.md)         | <span data-ttu-id="70b14-136">Carga una serie de glifos en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70b14-136">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="70b14-137">**PreloadText**</span><span class="sxs-lookup"><span data-stu-id="70b14-137">**PreloadText**</span></span>](id3dxfont--preloadtext.md)             | <span data-ttu-id="70b14-138">Carga texto con formato en la memoria de vídeo para mejorar la eficacia de la representación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70b14-138">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="70b14-139">Este método admite cadenas ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="70b14-139">This method supports ANSI and Unicode strings.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="70b14-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70b14-140">Remarks</span></span>

<span data-ttu-id="70b14-141">La interfaz **ID3DXFont** se obtiene llamando a [**D3DXCreateFont**](d3dxcreatefont.md) o [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span><span class="sxs-lookup"><span data-stu-id="70b14-141">The **ID3DXFont** interface is obtained by calling [**D3DXCreateFont**](d3dxcreatefont.md) or [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).</span></span>

<span data-ttu-id="70b14-142">El tipo LPD3DXFONT se define como un puntero a la interfaz **ID3DXFont** .</span><span class="sxs-lookup"><span data-stu-id="70b14-142">The LPD3DXFONT type is defined as a pointer to the **ID3DXFont** interface.</span></span>


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a><span data-ttu-id="70b14-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70b14-143">Requirements</span></span>



| <span data-ttu-id="70b14-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b14-144">Requirement</span></span> | <span data-ttu-id="70b14-145">Value</span><span class="sxs-lookup"><span data-stu-id="70b14-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70b14-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70b14-146">Header</span></span><br/>  | <dl> <span data-ttu-id="70b14-147"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="70b14-147"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="70b14-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70b14-148">Library</span></span><br/> | <dl> <span data-ttu-id="70b14-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70b14-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70b14-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="70b14-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b14-151">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="70b14-151">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
