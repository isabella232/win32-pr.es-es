---
title: Métodos de AddFontFaceReference de IDWriteFontSetBuilder (Dwrite \_ 3. h)
description: Agrega una referencia a una fuente al conjunto que se está compilando.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Métodos AddFontFaceReference de escritura directa
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690606"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="2b64f-104">IDWriteFontSetBuilder:: AddFontFaceReference (métodos)</span><span class="sxs-lookup"><span data-stu-id="2b64f-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="2b64f-105">Agrega una referencia a una fuente al conjunto que se está compilando.</span><span class="sxs-lookup"><span data-stu-id="2b64f-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2b64f-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="2b64f-106">Overload list</span></span>



| <span data-ttu-id="2b64f-107">Método</span><span class="sxs-lookup"><span data-stu-id="2b64f-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="2b64f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b64f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b64f-109">[**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="2b64f-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="2b64f-110">Agrega una referencia a una fuente al conjunto que se está compilando.</span><span class="sxs-lookup"><span data-stu-id="2b64f-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="2b64f-111">Los metadatos necesarios se extraerán automáticamente de la fuente al llamar a CreateFontSet.</span><span class="sxs-lookup"><span data-stu-id="2b64f-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2b64f-112">[**AddFontFaceReference (IDWriteFontFaceReference \* , const DWRITE \_ Font \_ propiedad \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="2b64f-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="2b64f-113">Agrega una referencia a una fuente al conjunto que se está compilando.</span><span class="sxs-lookup"><span data-stu-id="2b64f-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="2b64f-114">El autor de la llamada proporciona información suficiente para buscar, evitando la necesidad de abrir la fuente potencialmente no local.</span><span class="sxs-lookup"><span data-stu-id="2b64f-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="2b64f-115">Faltan las propiedades proporcionadas por el autor de la llamada y dichas propiedades no estarán disponibles como filtros en GetMatchingFonts.</span><span class="sxs-lookup"><span data-stu-id="2b64f-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="2b64f-116">GetPropertyValues las propiedades que faltan devolverán una lista de cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="2b64f-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="2b64f-117">Las propiedades que se pasan generalmente deben ser coherentes con el contenido real de la fuente, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2b64f-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="2b64f-118">Por ejemplo, puede asignar un alias a una fuente con un nombre diferente o un identificador único, o bien puede establecer etiquetas personalizadas que no estén presentes en la fuente real.</span><span class="sxs-lookup"><span data-stu-id="2b64f-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2b64f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b64f-119">Requirements</span></span>



| <span data-ttu-id="2b64f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b64f-120">Requirement</span></span> | <span data-ttu-id="2b64f-121">Value</span><span class="sxs-lookup"><span data-stu-id="2b64f-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b64f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b64f-122">Header</span></span><br/> | <dl> <span data-ttu-id="2b64f-123"><dt>Dwrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b64f-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b64f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b64f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b64f-125">**IDWriteFontSetBuilder**</span><span class="sxs-lookup"><span data-stu-id="2b64f-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="2b64f-126">�</span><span class="sxs-lookup"><span data-stu-id="2b64f-126">�</span></span>

<span data-ttu-id="2b64f-127">�</span><span class="sxs-lookup"><span data-stu-id="2b64f-127">�</span></span>
