---
title: Métodos ID2D1SvgElement GetAttributeValue
description: Obtiene un atributo de este elemento.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Métodos de GetAttributeValue Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 85e31a8efb1e39d47ab3959fc5ecc175336ab7b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078010"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>ID2D1SvgElement:: GetAttributeValue (métodos)

Obtiene un atributo de este elemento.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                     | Descripción                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue (PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Obtiene un atributo de este elemento como un valor de tipo float.<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR, D2D1 \_ color \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Obtiene un atributo de este elemento como un color.<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Obtiene un atributo de este elemento como un tipo de interfaz. <br/>                                                                                         |
| [**GetAttributeValue (PCWSTR, \_ modo de relleno D2D1 \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Obtiene un atributo de este elemento como modo de relleno. Este método se puede usar para obtener el valor de las propiedades de la regla de relleno o de la regla de recorte.<br/>             |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Obtiene un atributo de este elemento como una pintura. Este método se puede utilizar para obtener el valor de las propiedades Fill o Stroke.<br/>                         |
| [**GetAttributeValue (PCWSTR, \_ longitud D2D1 \_ SVG \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Obtiene un atributo de este elemento como un valor de longitud.<br/>                                                                                             |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Display \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Obtiene un atributo de este elemento como valor para mostrar. Este método se puede utilizar para obtener el valor de la propiedad display.<br/>                          |
| [**GetAttributeValue (PCWSTR, D2D1 \_ Extend \_ Mode \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Obtiene un atributo de este elemento como un valor de modo de extensión. Este método se puede usar para obtener el valor de un atributo spreadMethod.<br/>                  |
| [**GetAttributeValue (PCWSTR, desbordamiento de SVG de D2D1 \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Obtiene un atributo de este elemento como un valor de desbordamiento. Este método se puede utilizar para obtener el valor de la propiedad Overflow.<br/>                       |
| [**GetAttributeValue (PCWSTR, D2D1 \_ \_ extremo de línea SVG \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Obtiene un atributo de este elemento como un valor de extremo de línea. Este método se puede usar para obtener el valor de la propiedad stroke-LineCap.<br/>                  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Obtiene un atributo de este elemento como un valor de matriz. Este método se puede utilizar para obtener el valor de un atributo Transform o gradientTransform.<br/>     |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Obtiene un atributo de este elemento como datos de la ruta de acceso. Este método se puede utilizar para obtener el valor del atributo d en un elemento path.<br/>                   |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ line \_ join \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Obtiene un atributo de este elemento como un valor de combinación de línea. Este método se puede usar para obtener el valor de la propiedad stroke-LineJoin.<br/>                |
| [**GetAttributeValue (PCWSTR, D2D1 \_ \_ tipo de unidad SVG \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Obtiene un atributo de este elemento como un valor de tipo de unidad. Este método se puede usar para obtener el valor de un atributo gradientUnits o clipPathUnits.<br/>  |
| [**GetAttributeValue (PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Obtiene un atributo de este elemento.<br/>                                                                                                               |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Visibility \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Obtiene un atributo de este elemento como un valor de visibilidad. Este método se puede utilizar para obtener el valor de la propiedad Visibility.<br/>                    |
| [**GetAttributeValue (PCWSTR, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Obtiene un atributo de este elemento como una matriz de guiones de trazo. Este método se puede usar para obtener el valor de la propiedad stroke-dasharray.<br/>             |
| [**GetAttributeValue (PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Obtiene un atributo de este elemento como puntos. Este método se puede utilizar para obtener el valor del atributo Points en un elemento Polygon o Polyline.<br/>  |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ conservar \_ relación de aspecto \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Obtiene un atributo de este elemento como un valor de la relación de aspecto de conservación. Este método se puede usar para obtener el valor de un atributo preserveAspectRatio.<br/> |
| [**GetAttributeValue (PCWSTR, D2D1 \_ SVG \_ Attribute \_ Pod \_ Type, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Obtiene un atributo de este elemento como un tipo POD.<br/>                                                                                                 |
| [**GetAttributeValue (PCWSTR, D2D1 \_ \_ tipo cadena de atributo SVG \_ \_ , PWSTR, UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Obtiene un atributo de este elemento como una cadena. <br/>                                                                                                  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

