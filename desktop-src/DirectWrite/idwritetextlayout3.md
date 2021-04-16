---
title: Interfaz IDWriteTextLayout3
description: Representa un bloque de texto una vez que se ha analizado y formateado por completo. | Interfaz IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Interfaz IDWriteTextLayout3 de escritura directa
- IDWriteTextLayout3 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670181"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="c2fbe-106">Interfaz IDWriteTextLayout3</span><span class="sxs-lookup"><span data-stu-id="c2fbe-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="c2fbe-107">Representa un bloque de texto una vez que se ha analizado y formateado por completo.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="c2fbe-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2fbe-108">Members</span></span>

<span data-ttu-id="c2fbe-109">La interfaz **IDWriteTextLayout3** hereda de [**IDWriteTextLayout2**](idwritetextlayout2.md).</span><span class="sxs-lookup"><span data-stu-id="c2fbe-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="c2fbe-110">**IDWriteTextLayout3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2fbe-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="c2fbe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2fbe-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c2fbe-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2fbe-112">Methods</span></span>

<span data-ttu-id="c2fbe-113">La interfaz **IDWriteTextLayout3** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="c2fbe-114">Método</span><span class="sxs-lookup"><span data-stu-id="c2fbe-114">Method</span></span>                                                          | <span data-ttu-id="c2fbe-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2fbe-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2fbe-116">**GetLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="c2fbe-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="c2fbe-117">Recupera las propiedades de cada línea.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="c2fbe-118">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="c2fbe-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="c2fbe-119">Obtiene la información de espaciado de línea.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="c2fbe-120">**InvalidateLayout**</span><span class="sxs-lookup"><span data-stu-id="c2fbe-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="c2fbe-121">Invalida el diseño, forzando el diseño para que se remedie antes de llamar a las métricas o funciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="c2fbe-122">Esto resulta útil si el emplazamiento de una fuente cambia y el diseño debe volver a dibujarse, o si el tamaño de un cliente implementa IDWriteInlineObject cambios.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="c2fbe-123">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="c2fbe-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="c2fbe-124">Establezca el interlineado.</span><span class="sxs-lookup"><span data-stu-id="c2fbe-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="c2fbe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2fbe-125">Requirements</span></span>



| <span data-ttu-id="c2fbe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2fbe-126">Requirement</span></span> | <span data-ttu-id="c2fbe-127">Value</span><span class="sxs-lookup"><span data-stu-id="c2fbe-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fbe-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2fbe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2fbe-129">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="c2fbe-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="c2fbe-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2fbe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2fbe-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c2fbe-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c2fbe-132">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2fbe-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c2fbe-133">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="c2fbe-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="c2fbe-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2fbe-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2fbe-135"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2fbe-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c2fbe-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2fbe-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2fbe-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2fbe-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2fbe-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2fbe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2fbe-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="c2fbe-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





