---
description: Describe cómo un parámetro (método o evento) almacena su valor.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Enumeración WpdParameterAttributeForm (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f50665768d62d8155bd0ac9001f4ae5029766d7d5b27a942941f8f41b9492e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026753"
---
# <a name="wpdparameterattributeform-enumeration"></a>WpdParameterAttributeForm (enumeración)

El [**tipo de enumeración WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) describe cómo un parámetro (método o evento) almacena su valor.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**FORMULARIO DE \_ ATRIBUTO \_ DE PARÁMETRO \_ WPD SIN \_ ESPECIFICAR**
</dt> <dd>

No se especifica el formato del parámetro.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**INTERVALO DE FORMULARIO \_ DEL ATRIBUTO DE PARÁMETRO \_ \_ \_ WPD**
</dt> <dd>

El parámetro especifica un intervalo.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**ENUMERACIÓN DE FORMULARIO \_ DE ATRIBUTO DE PARÁMETRO \_ \_ \_ WPD**
</dt> <dd>

El parámetro es una enumeración.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**EXPRESIÓN REGULAR \_ DEL ATRIBUTO DE PARÁMETRO \_ \_ \_ WPD \_**
</dt> <dd>

El parámetro es una expresión regular.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**IDENTIFICADOR DE OBJETO \_ DE ATRIBUTO DE PARÁMETRO \_ \_ \_ WPD**
</dt> <dd>

El parámetro es un identificador de objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

