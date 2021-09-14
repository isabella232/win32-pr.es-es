---
title: Elemento HeaderFields (sendEmailType)
description: Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Elemento HeaderFields Programador de tareas
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259316"
---
# <a name="headerfields-sendemailtype-element"></a>Elemento HeaderFields (sendEmailType)

Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **HeaderFields.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Tipo                                                                       | Descripción                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Contiene un campo para un encabezado en un mensaje de correo electrónico. <br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea Propiedad HeaderFields de IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)

Para el desarrollo de scripts, [**vea EmailAction.HeaderFields.**](emailaction-headerfields.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





