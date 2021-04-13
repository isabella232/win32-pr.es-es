---
title: Interfaz IDWriteTextLayout2
description: Representa un bloque de texto una vez que se ha analizado y formateado por completo. | Interfaz IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Interfaz IDWriteTextLayout2 de escritura directa
- IDWriteTextLayout2 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362255"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="878f1-106">Interfaz IDWriteTextLayout2</span><span class="sxs-lookup"><span data-stu-id="878f1-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="878f1-107">Representa un bloque de texto una vez que se ha analizado y formateado por completo.</span><span class="sxs-lookup"><span data-stu-id="878f1-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="878f1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="878f1-108">Members</span></span>

<span data-ttu-id="878f1-109">La interfaz **IDWriteTextLayout2** hereda de [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span><span class="sxs-lookup"><span data-stu-id="878f1-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="878f1-110">**IDWriteTextLayout2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="878f1-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="878f1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="878f1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="878f1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="878f1-112">Methods</span></span>

<span data-ttu-id="878f1-113">La interfaz **IDWriteTextLayout2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="878f1-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="878f1-114">Método</span><span class="sxs-lookup"><span data-stu-id="878f1-114">Method</span></span>                                                                                | <span data-ttu-id="878f1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="878f1-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="878f1-116">**GetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="878f1-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="878f1-117">Obtiene el objeto de reserva de fuente actual.</span><span class="sxs-lookup"><span data-stu-id="878f1-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="878f1-118">**GetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="878f1-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="878f1-119">Obtiene si se ajusta o no la última palabra de la última línea.</span><span class="sxs-lookup"><span data-stu-id="878f1-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="878f1-120">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="878f1-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="878f1-121">Recupera las métricas generales de la cadena con formato.</span><span class="sxs-lookup"><span data-stu-id="878f1-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="878f1-122">**GetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="878f1-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="878f1-123">Obtiene el modo en que los glifos se alinean con los bordes del margen.</span><span class="sxs-lookup"><span data-stu-id="878f1-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="878f1-124">**GetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="878f1-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="878f1-125">Obtiene la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.</span><span class="sxs-lookup"><span data-stu-id="878f1-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="878f1-126">**SetFontFallback**</span><span class="sxs-lookup"><span data-stu-id="878f1-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="878f1-127">Aplicar una reserva de fuentes personalizada en el diseño.</span><span class="sxs-lookup"><span data-stu-id="878f1-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="878f1-128">**SetLastLineWrapping**</span><span class="sxs-lookup"><span data-stu-id="878f1-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="878f1-129">Establece si se ajusta o no la última palabra de la última línea.</span><span class="sxs-lookup"><span data-stu-id="878f1-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="878f1-130">**SetOpticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="878f1-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="878f1-131">Establece cómo se alinean los glifos con los bordes del margen.</span><span class="sxs-lookup"><span data-stu-id="878f1-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="878f1-132">**SetVerticalGlyphOrientation**</span><span class="sxs-lookup"><span data-stu-id="878f1-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="878f1-133">Establecer la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.</span><span class="sxs-lookup"><span data-stu-id="878f1-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="878f1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="878f1-134">Requirements</span></span>



| <span data-ttu-id="878f1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="878f1-135">Requirement</span></span> | <span data-ttu-id="878f1-136">Value</span><span class="sxs-lookup"><span data-stu-id="878f1-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="878f1-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="878f1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="878f1-138">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="878f1-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="878f1-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="878f1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="878f1-140">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="878f1-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="878f1-141">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="878f1-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="878f1-142">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="878f1-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="878f1-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="878f1-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="878f1-144"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="878f1-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="878f1-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="878f1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="878f1-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="878f1-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="878f1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="878f1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878f1-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="878f1-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

