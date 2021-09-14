---
title: Métodos ID2D1SvgElement GetAttributeValue
description: Obtiene un atributo de este elemento.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Métodos GetAttributeValue de Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 85e31a8efb1e39d47ab3959fc5ecc175336ab7b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162766"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>Métodos ID2D1SvgElement::GetAttributeValue

Obtiene un atributo de este elemento.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                     | Descripción                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue(PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Obtiene un atributo de este elemento como float.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Obtiene un atributo de este elemento como color.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Obtiene un atributo de este elemento como un tipo de interfaz. <br/>                                                                                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Obtiene un atributo de este elemento como modo de relleno. Este método se puede usar para obtener el valor de las propiedades fill-rule o clip-rule.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Obtiene un atributo de este elemento como una pintura. Este método se puede usar para obtener el valor de las propiedades de relleno o trazo.<br/>                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Obtiene un atributo de este elemento como un valor de longitud.<br/>                                                                                             |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Obtiene un atributo de este elemento como un valor para mostrar. Este método se puede usar para obtener el valor de la propiedad para mostrar.<br/>                          |
| [**GetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Obtiene un atributo de este elemento como un valor de modo de extensión. Este método se puede usar para obtener el valor de un atributo spreadMethod.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Obtiene un atributo de este elemento como un valor de desbordamiento. Este método se puede usar para obtener el valor de la propiedad overflow.<br/>                       |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE CAP \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Obtiene un atributo de este elemento como un valor de extremo de línea. Este método se puede usar para obtener el valor de la propiedad stroke-linecap.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Obtiene un atributo de este elemento como un valor de matriz. Este método se puede usar para obtener el valor de un atributo transform o gradientTransform.<br/>     |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Obtiene un atributo de este elemento como datos de ruta de acceso. Este método se puede usar para obtener el valor del atributo d en un elemento path.<br/>                   |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE JOIN \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Obtiene un atributo de este elemento como un valor de combinación de línea. Este método se puede usar para obtener el valor de la propiedad stroke-linejoin.<br/>                |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT TYPE \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Obtiene un atributo de este elemento como un valor de tipo de unidad. Este método se puede usar para obtener el valor de un atributo gradientUnits o clipPathUnits.<br/>  |
| [**GetAttributeValue(PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Obtiene un atributo de este elemento.<br/>                                                                                                               |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Obtiene un atributo de este elemento como un valor de visibilidad. Este método se puede usar para obtener el valor de la propiedad de visibilidad.<br/>                    |
| [**GetAttributeValue(PCWSTR, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Obtiene un atributo de este elemento como una matriz de guiones de trazo. Este método se puede usar para obtener el valor de la propiedad stroke-dasharray.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Obtiene un atributo de este elemento como puntos. Este método se puede usar para obtener el valor del atributo points en un elemento polilínea o polígono.<br/>  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG PRESERVE ASPECT RATIO \_ \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Obtiene un atributo de este elemento como un valor de relación de aspecto de conservación. Este método se puede usar para obtener el valor de un atributo preserveAspectRatio.<br/> |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Obtiene un atributo de este elemento como un tipo POD.<br/>                                                                                                 |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PWSTR, UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Obtiene un atributo de este elemento como una cadena. <br/>                                                                                                  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

