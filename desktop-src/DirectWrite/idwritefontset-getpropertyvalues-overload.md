---
title: Métodos IDWriteFontSet GetPropertyValues (Dwrite \_ 3.h)
description: Devuelve valores de propiedad para el conjunto de fuentes.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Métodos GetPropertyValues de Escritura directa
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816366"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Métodos IDWriteFontSet::GetPropertyValues

Devuelve valores de propiedad para el conjunto de fuentes.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Devuelve todos los valores de propiedad únicos del conjunto, que se pueden usar para fines como mostrar una lista de familias o una nube de etiquetas. Todos los valores se devuelven independientemente del idioma, incluidos todos los nombres localizados. <br/>                                                                                       |
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Devuelve todos los valores de propiedad únicos del conjunto, que se pueden usar para fines como mostrar una lista de familias o una nube de etiquetas. Los valores se devuelven en orden de prioridad según la lista de idiomas, de modo que si una fuente contiene más de un nombre localizado, se devolverá el preferido. <br/> |
| [**GetPropertyValues(UINT32, DWRITE \_ FONT \_ PROPERTY \_ ID, BOOL \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Devuelve los valores de propiedad de un índice de elemento de fuente específico.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
