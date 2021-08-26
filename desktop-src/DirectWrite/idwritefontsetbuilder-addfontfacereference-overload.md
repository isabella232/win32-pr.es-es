---
title: Métodos IdWriteFontSetBuilder AddFontFaceReference (Dwrite \_ 3.h)
description: Agrega una referencia a una fuente al conjunto que se está construyendo.
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
ms.openlocfilehash: c9edfed7680b18ef9ffb271cb59de3a54d4b408ac5f194a7bead1bbb3fb9b2ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075585"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>Métodos IDWriteFontSetBuilder::AddFontFaceReference

Agrega una referencia a una fuente al conjunto que se está construyendo.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference(IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Agrega una referencia a una fuente al conjunto que se está construyendo. Los metadatos necesarios se extraerán automáticamente de la fuente al llamar a CreateFontSet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference(IDWriteFontFaceReference \* , const DWRITE \_ FONT \_ PROPERTY \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Agrega una referencia a una fuente al conjunto que se está construyendo. El autor de la llamada proporciona suficiente información en la que buscar, lo que evita la necesidad de abrir la fuente potencialmente no local. Faltan las propiedades no proporcionadas por el autor de la llamada y esas propiedades no estarán disponibles como filtros en GetMatchingFonts. GetPropertyValues para las propiedades que faltan devolverá una lista de cadenas vacía. Por lo general, las propiedades pasadas deben ser coherentes con el contenido real de la fuente, pero no es necesario. Por ejemplo, podría asignar un alias a una fuente con un nombre o identificador único distintos, o bien podría establecer etiquetas personalizadas que no están presentes en la fuente real.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
