---
description: El tipo de enumeración WpdAttributeForm describe el modo en que una propiedad almacena sus valores.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumeración WpdAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650187"
---
# <a name="wpdattributeform-enumeration"></a>Enumeración WpdAttributeForm

El tipo de enumeración **WpdAttributeForm** describe el modo en que una propiedad almacena sus valores.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**formulario de atributo de propiedad de WPD no \_ \_ \_ \_ especificado**
</dt> <dd>

No se especifica el formato de los datos de la propiedad.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_rango de \_ formulario de atributos de propiedad de WPD \_ \_**
</dt> <dd>

El valor se expresa como un intervalo de valores, con un mínimo y un máximo.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ \_ enumeración de formulario de atributo de propiedad de WPD \_**
</dt> <dd>

La propiedad tiene una serie de valores individuales.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ expresión regular del formulario de atributo \_ de propiedad de WPD \_**
</dt> <dd>

El valor de propiedad es una expresión regular, no una expresión literal.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_ \_ \_ identificador OJBECT del formulario de atributo \_ de propiedad de WPD \_**
</dt> <dd>

El valor de propiedad representa un identificador de objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la propiedad del formulario de atributo de propiedad de WPD para describir cómo se almacenan los datos de una propiedad. [ \_ \_ \_ ](attributes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




