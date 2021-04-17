---
title: Métodos ID2D1SvgElement SetAttributeValue (D2d1svg. h)
description: Establece un atributo de este elemento.
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- Métodos de SetAttributeValue Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c49f224d364523653e13fb7b6cc141e8e8c6eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690564"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>ID2D1SvgElement:: SetAttributeValue (métodos)

Establece un atributo de este elemento.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                      | Descripción                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAttributeValue (PCWSTR, FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | Establece un atributo de este elemento mediante un valor de tipo float.<br/>                                                                                                 |
| [**SetAttributeValue (PCWSTR, D2D1 \_ color \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | Establece un atributo de este elemento como un color.<br/>                                                                                                    |
| [**SetAttributeValue (PCWSTR, \_ modo de relleno D2D1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | Establece un atributo de este elemento como modo de relleno. Este método se puede usar para establecer el valor de las propiedades ' Fill-rule ' o ' clip-rule '.<br/>         |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Display)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | Obtiene un atributo de este elemento como valor para mostrar. Este método se puede utilizar para obtener el valor de la propiedad display.<br/>                          |
| [**SetAttributeValue (PCWSTR, D2D1 \_ Extend \_ Mode)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | Establece un atributo de este elemento como un valor de modo de extensión. Este método se puede utilizar para establecer el valor de un atributo spreadMethod.<br/>                 |
| [**SetAttributeValue (PCWSTR, desbordamiento de SVG de D2D1 \_ \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | Establece un atributo de este elemento como un valor de desbordamiento. Este método se puede utilizar para establecer el valor de la propiedad Overflow.<br/>                       |
| [**SetAttributeValue (PCWSTR, D2D1 \_ \_ extremo de línea SVG \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | Establece un atributo de este elemento como un valor de extremo de línea. Este método se puede usar para establecer el valor de la propiedad stroke-LineCap.<br/>                  |
| [**SetAttributeValue (PCWSTR, D2D1 \_ longitud de SVG \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | Establece un atributo de este elemento como un valor de longitud.<br/>                                                                                             |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ line \_ join)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | Establece un atributo de este elemento como un valor de combinación de línea. Este método se puede utilizar para establecer el valor de la propiedad stroke-LineJoin.<br/>                |
| [**SetAttributeValue (PCWSTR, D2D1 \_ \_ tipo de unidad SVG \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | Establece un atributo de este elemento como un valor de tipo de unidad. Este método se puede utilizar para establecer el valor de un atributo gradientUnits o clipPathUnits.<br/>  |
| [**SetAttributeValue (PCWSTR, ID2D1SvgAttribute \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | Establece un atributo de este elemento mediante una interfaz.<br/>                                                                                            |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Visibility)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | Establece un atributo de este elemento como un valor de visibilidad. Este método se puede utilizar para establecer el valor de la propiedad Visibility.<br/>                    |
| [**SetAttributeValue (PCWSTR, D2D1 \_ Matrix \_ 3X2 \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | Establece un atributo de este elemento como un valor de matriz. Este método se puede utilizar para establecer el valor de un atributo Transform o gradientTransform.<br/>     |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ conservar \_ relación de aspecto \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | Establece un atributo de este elemento como un valor de la relación de aspecto de conservación. Este método se puede utilizar para establecer el valor de un atributo preserveAspectRatio.<br/> |
| [**SetAttributeValue (PCWSTR, D2D1 \_ \_ tipo de cadena de atributo SVG \_ \_ , PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | Establece un atributo de este elemento mediante una cadena. <br/>                                                                                               |
| [**SetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Attribute \_ Pod \_ Type, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | Establece un atributo de este elemento mediante un tipo POD.<br/>                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1svg. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
