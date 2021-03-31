---
title: ReplyTo (sendEmailType) (elemento)
description: Contiene las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- Elemento ReplyTo Programador de tareas
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151178"
---
# <a name="replyto-sendemailtype-element"></a>ReplyTo (sendEmailType) (elemento)

Contiene las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

El elemento **ReplyTo** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, consulte la [**propiedad ReplyTo de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).

Para el desarrollo de scripts, vea [**EmailAction. ReplyTo**](emailaction-replyto.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





