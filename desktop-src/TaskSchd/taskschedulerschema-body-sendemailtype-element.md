---
title: Elemento Body (sendEmailType)
description: Contiene el texto en el cuerpo del mensaje de correo electrónico.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Elemento body Programador de tareas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160606"
---
# <a name="body-sendemailtype-element"></a>Elemento Body (sendEmailType)

Contiene el texto en el cuerpo del mensaje de correo electrónico.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **Body.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Para el desarrollo de scripts, [**vea EmailAction.Body**](emailaction-body.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





