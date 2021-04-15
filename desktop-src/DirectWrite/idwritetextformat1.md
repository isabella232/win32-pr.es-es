---
title: Interfaz IDWriteTextFormat1
description: Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional. | Interfaz IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Interfaz IDWriteTextFormat1 de escritura directa
- IDWriteTextFormat1 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670124"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="312cf-106">Interfaz IDWriteTextFormat1</span><span class="sxs-lookup"><span data-stu-id="312cf-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="312cf-107">Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="312cf-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="312cf-108">Esta interfaz tiene los mismos métodos que [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y agrega la posibilidad de aplicar una orientación explícita.</span><span class="sxs-lookup"><span data-stu-id="312cf-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="312cf-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="312cf-109">Members</span></span>

<span data-ttu-id="312cf-110">La interfaz **IDWriteTextFormat1** hereda de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="312cf-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="312cf-111">**IDWriteTextFormat1** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="312cf-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="312cf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="312cf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="312cf-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="312cf-113">Methods</span></span>

<span data-ttu-id="312cf-114">La interfaz **IDWriteTextFormat1** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="312cf-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="312cf-115">Método</span><span class="sxs-lookup"><span data-stu-id="312cf-115">Method</span></span>                                                                                | <span data-ttu-id="312cf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="312cf-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="312cf-117">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="312cf-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="312cf-118">Obtiene la reserva actual.</span><span class="sxs-lookup"><span data-stu-id="312cf-118">Gets the current fallback.</span></span> <span data-ttu-id="312cf-119">Si nunca se ha establecido ninguna desde la creación del diseño, será nullptr.</span><span class="sxs-lookup"><span data-stu-id="312cf-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="312cf-120">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="312cf-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="312cf-121">Obtiene el modo de ajuste de la última línea.</span><span class="sxs-lookup"><span data-stu-id="312cf-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="312cf-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="312cf-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="312cf-123">Obtiene la alineación del margen óptico para el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="312cf-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="312cf-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="312cf-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="312cf-125">Obtiene la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.</span><span class="sxs-lookup"><span data-stu-id="312cf-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="312cf-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="312cf-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="312cf-127">Aplica la reserva de fuentes personalizada en el diseño.</span><span class="sxs-lookup"><span data-stu-id="312cf-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="312cf-128">Si no se establece ninguno, se usa la lista de reserva predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="312cf-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="312cf-129">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="312cf-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="312cf-130">Establece el modo de ajuste de la última línea.</span><span class="sxs-lookup"><span data-stu-id="312cf-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="312cf-131">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="312cf-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="312cf-132">Establece la alineación del margen óptico para el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="312cf-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="312cf-133">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="312cf-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="312cf-134">Establece la orientación de un formato de texto.</span><span class="sxs-lookup"><span data-stu-id="312cf-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="312cf-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="312cf-135">Requirements</span></span>



| <span data-ttu-id="312cf-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="312cf-136">Requirement</span></span> | <span data-ttu-id="312cf-137">Value</span><span class="sxs-lookup"><span data-stu-id="312cf-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="312cf-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312cf-138">Minimum supported client</span></span><br/> | <span data-ttu-id="312cf-139">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="312cf-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="312cf-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312cf-140">Minimum supported server</span></span><br/> | <span data-ttu-id="312cf-141">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="312cf-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="312cf-142">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="312cf-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="312cf-143">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="312cf-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="312cf-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="312cf-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="312cf-145"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="312cf-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="312cf-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="312cf-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="312cf-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="312cf-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="312cf-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="312cf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312cf-149">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="312cf-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

