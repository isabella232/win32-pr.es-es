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
ms.openlocfilehash: 2af801385c74fa26221556b713faf8db915037ef4cf7439d71a2e2d4004193d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100035"
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



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad HeaderFields de IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)

Para el desarrollo de scripts, [**vea EmailAction.HeaderFields.**](emailaction-headerfields.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





