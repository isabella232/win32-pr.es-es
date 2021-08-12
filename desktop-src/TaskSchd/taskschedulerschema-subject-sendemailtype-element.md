---
title: Elemento Subject (sendEmailType)
description: Contiene el asunto del mensaje de correo electrónico.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Elemento Subject Programador de tareas
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15bf3c84befd9dd8f4c9c4a544fc920b7066184c6bf367c404bb14f22f573b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611193"
---
# <a name="subject-sendemailtype-element"></a>Elemento Subject (sendEmailType)

Contiene el asunto del mensaje de correo electrónico.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **Subject.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).

Para el desarrollo de scripts, [**vea EmailAction.Subject.**](emailaction-subject.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





