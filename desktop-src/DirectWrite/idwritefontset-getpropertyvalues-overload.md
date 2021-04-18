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
# <a name="idwritefontsetgetpropertyvalues-methods"></a>IDWriteFontSet:: GetPropertyValues (métodos)

Devuelve los valores de propiedad del conjunto de fuentes.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues ( \_ \_ identificador de la propiedad de fuente DWRITE \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Devuelve todos los valores de propiedad únicos del conjunto, que se pueden usar para fines como mostrar una lista de familia o una nube de etiquetas. Todos los valores se devuelven independientemente del idioma, incluidos todos los nombres localizados. <br/>                                                                                       |
| [**GetPropertyValues ( \_ \_ identificador de la propiedad de fuente DWRITE \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Devuelve todos los valores de propiedad únicos del conjunto, que se pueden usar para fines como mostrar una lista de familia o una nube de etiquetas. Los valores se devuelven en orden de prioridad según la lista de idiomas, de modo que si una fuente contiene más de un nombre localizado, se devolverá el preferido. <br/> |
| [**GetPropertyValues (UINT32, DWRITE \_ \_ \_ ID. de propiedad de fuente, bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Devuelve los valores de propiedad de un índice de elemento de fuente específico.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dwrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
