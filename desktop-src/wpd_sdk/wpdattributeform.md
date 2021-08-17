---
description: El tipo de enumeración WpdAttributeForm describe cómo una propiedad almacena sus valores.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumeración WpdAttributeForm (PortableDevice.h)
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
ms.openlocfilehash: 8366f90fe41eaa92d826f4d761fe8cdf58304f54e1f57cb074ae94d6fd9f1ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696283"
---
# <a name="wpdattributeform-enumeration"></a>WpdAttributeForm (enumeración)

El **tipo de enumeración WpdAttributeForm** describe cómo una propiedad almacena sus valores.

## <a name="syntax"></a>Syntax


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

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**FORMULARIO DE \_ ATRIBUTO \_ DE PROPIEDAD \_ WPD SIN \_ ESPECIFICAR**
</dt> <dd>

No se especifica el formato de los datos de la propiedad.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**INTERVALO DE \_ FORMULARIOS DE \_ ATRIBUTO DE \_ PROPIEDAD \_ WPD**
</dt> <dd>

El valor se expresa como un intervalo de valores, con un mínimo y un máximo.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**ENUMERACIÓN DE FORMULARIO \_ DE ATRIBUTO DE PROPIEDAD \_ \_ WPD \_**
</dt> <dd>

La propiedad tiene una serie de valores individuales.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**EXPRESIÓN REGULAR \_ DEL ATRIBUTO DE PROPIEDAD \_ \_ \_ WPD \_**
</dt> <dd>

El valor de propiedad es una expresión regular, no una expresión literal.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD \_ PROPERTY \_ ATTRIBUTE \_ FORM \_ OJBECT \_ IDENTIFIER**
</dt> <dd>

El valor de propiedad representa un identificador de objeto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la [propiedad \_ WPD PROPERTY \_ ATTRIBUTE \_ FORM](attributes.md) para describir cómo se almacenan los datos de una propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




