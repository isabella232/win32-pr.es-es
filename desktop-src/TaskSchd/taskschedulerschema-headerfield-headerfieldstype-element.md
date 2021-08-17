---
title: Elemento HeaderField (headerFieldsType)
description: Contiene un campo para un encabezado en un mensaje de correo electrónico.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Elemento HeaderField Programador de tareas
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918e432ce7a8ea2d43769b9d9ee1315a4b35bce6f2c0cb23f1153ec7afe1a599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139218"
---
# <a name="headerfield-headerfieldstype-element"></a>Elemento HeaderField (headerFieldsType)

Contiene un campo para un encabezado en un mensaje de correo electrónico.

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

El **elemento HeaderField** se define mediante el tipo [**complejo headerFieldsType.**](taskschedulerschema-headerfieldstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                        | Derivado de                                                                 | Descripción                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Especifica los campos de encabezado y sus valores usados en el encabezado del mensaje de correo electrónico.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                            | Tipo                                                                    | Descripción                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nombre**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica el nombre del campo de encabezado en un mensaje de correo electrónico.<br/> |
| [**Value**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Especifica el valor de un campo de encabezado en un mensaje de correo electrónico.<br/>  |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad HeaderFields de IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)

Para el desarrollo de scripts, [**vea EmailAction.HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





