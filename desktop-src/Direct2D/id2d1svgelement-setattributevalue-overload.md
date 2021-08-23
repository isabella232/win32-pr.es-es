---
title: Métodos SetAttributeValue de ID2D1SvgElement (D2d1svg.h)
description: Establece un atributo de este elemento.
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- Métodos SetAttributeValue de Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 95ac3021abdf641b268e2278e92dfd86227244cde1d1d51f992953e68584fa69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527145"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>Métodos ID2D1SvgElement::SetAttributeValue

Establece un atributo de este elemento.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                      | Descripción                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAttributeValue(PCWSTR, FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | Establece un atributo de este elemento mediante float.<br/>                                                                                                 |
| [**SetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | Establece un atributo de este elemento como color.<br/>                                                                                                    |
| [**SetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | Establece un atributo de este elemento como modo de relleno. Este método se puede usar para establecer el valor de las propiedades "fill-rule" o "clip-rule".<br/>         |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | Obtiene un atributo de este elemento como un valor para mostrar. Este método se puede usar para obtener el valor de la propiedad para mostrar.<br/>                          |
| [**SetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | Establece un atributo de este elemento como un valor de modo de extensión. Este método se puede usar para establecer el valor de un atributo spreadMethod.<br/>                 |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | Establece un atributo de este elemento como un valor de desbordamiento. Este método se puede usar para establecer el valor de la propiedad de desbordamiento.<br/>                       |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ CAP)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | Establece un atributo de este elemento como un valor de extremo de línea. Este método se puede usar para establecer el valor de la propiedad stroke-linecap.<br/>                  |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | Establece un atributo de este elemento como un valor de longitud.<br/>                                                                                             |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ JOIN)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | Establece un atributo de este elemento como un valor de combinación de línea. Este método se puede usar para establecer el valor de la propiedad stroke-linejoin.<br/>                |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT \_ TYPE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | Establece un atributo de este elemento como un valor de tipo de unidad. Este método se puede usar para establecer el valor de un atributo gradientUnits o clipPathUnits.<br/>  |
| [**SetAttributeValue(PCWSTR, ID2D1SvgAttribute \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | Establece un atributo de este elemento mediante una interfaz .<br/>                                                                                            |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | Establece un atributo de este elemento como un valor de visibilidad. Este método se puede usar para establecer el valor de la propiedad de visibilidad.<br/>                    |
| [**SetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | Establece un atributo de este elemento como un valor de matriz. Este método se puede usar para establecer el valor de un atributo transform o gradientTransform.<br/>     |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG PRESERVE ASPECT RATIO \_ \_ \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | Establece un atributo de este elemento como un valor de relación de aspecto de conservación. Este método se puede usar para establecer el valor de un atributo preserveAspectRatio.<br/> |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | Establece un atributo de este elemento mediante una cadena. <br/>                                                                                               |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE , void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | Establece un atributo de este elemento mediante un tipo POD.<br/>                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1svg.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
