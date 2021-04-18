---
title: Métodos de GetPropertyValues de IDWriteFontSet (Dwrite \_ 3. h)
description: Devuelve los valores de propiedad del conjunto de fuentes.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Métodos GetPropertyValues de escritura directa
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670864"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="2c317-104">IDWriteFontSet:: GetPropertyValues (métodos)</span><span class="sxs-lookup"><span data-stu-id="2c317-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="2c317-105">Devuelve los valores de propiedad del conjunto de fuentes.</span><span class="sxs-lookup"><span data-stu-id="2c317-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2c317-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="2c317-106">Overload list</span></span>



| <span data-ttu-id="2c317-107">Método</span><span class="sxs-lookup"><span data-stu-id="2c317-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="2c317-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c317-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c317-109">[**GetPropertyValues ( \_ \_ identificador de la propiedad de fuente DWRITE \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="2c317-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="2c317-110">Devuelve todos los valores de propiedad únicos del conjunto, que se pueden usar para fines como mostrar una lista de familia o una nube de etiquetas.</span><span class="sxs-lookup"><span data-stu-id="2c317-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="2c317-111">Todos los valores se devuelven independientemente del idioma, incluidos todos los nombres localizados.</span><span class="sxs-lookup"><span data-stu-id="2c317-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="2c317-112">[**GetPropertyValues ( \_ \_ identificador de la propiedad de fuente DWRITE \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="2c317-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="2c317-113">Devuelve todos los valores de propiedad únicos del conjunto, que se pueden usar para fines como mostrar una lista de familia o una nube de etiquetas.</span><span class="sxs-lookup"><span data-stu-id="2c317-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="2c317-114">Los valores se devuelven en orden de prioridad según la lista de idiomas, de modo que si una fuente contiene más de un nombre localizado, se devolverá el preferido.</span><span class="sxs-lookup"><span data-stu-id="2c317-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="2c317-115">[**GetPropertyValues (UINT32, DWRITE \_ \_ \_ ID. de propiedad de fuente, bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="2c317-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="2c317-116">Devuelve los valores de propiedad de un índice de elemento de fuente específico.</span><span class="sxs-lookup"><span data-stu-id="2c317-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="2c317-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c317-117">Requirements</span></span>



| <span data-ttu-id="2c317-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c317-118">Requirement</span></span> | <span data-ttu-id="2c317-119">Value</span><span class="sxs-lookup"><span data-stu-id="2c317-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c317-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c317-120">Header</span></span><br/> | <dl> <span data-ttu-id="2c317-121"><dt>Dwrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c317-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c317-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c317-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c317-123">**IDWriteFontSet**</span><span class="sxs-lookup"><span data-stu-id="2c317-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="2c317-124">�</span><span class="sxs-lookup"><span data-stu-id="2c317-124">�</span></span>

<span data-ttu-id="2c317-125">�</span><span class="sxs-lookup"><span data-stu-id="2c317-125">�</span></span>
