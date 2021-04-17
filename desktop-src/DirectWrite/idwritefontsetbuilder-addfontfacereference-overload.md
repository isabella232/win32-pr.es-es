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
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>IDWriteFontSetBuilder:: AddFontFaceReference (métodos)

Agrega una referencia a una fuente al conjunto que se está compilando.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Agrega una referencia a una fuente al conjunto que se está compilando. Los metadatos necesarios se extraerán automáticamente de la fuente al llamar a CreateFontSet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference (IDWriteFontFaceReference \* , const DWRITE \_ Font \_ propiedad \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Agrega una referencia a una fuente al conjunto que se está compilando. El autor de la llamada proporciona información suficiente para buscar, evitando la necesidad de abrir la fuente potencialmente no local. Faltan las propiedades proporcionadas por el autor de la llamada y dichas propiedades no estarán disponibles como filtros en GetMatchingFonts. GetPropertyValues las propiedades que faltan devolverán una lista de cadenas vacías. Las propiedades que se pasan generalmente deben ser coherentes con el contenido real de la fuente, pero no es necesario. Por ejemplo, puede asignar un alias a una fuente con un nombre diferente o un identificador único, o bien puede establecer etiquetas personalizadas que no estén presentes en la fuente real.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dwrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
