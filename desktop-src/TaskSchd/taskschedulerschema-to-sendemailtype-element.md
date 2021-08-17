---
title: Elemento To (sendEmailType)
description: Contiene las direcciones de correo electrónico a las que se enviará el correo electrónico.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- Elemento To Programador de tareas
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2367686e308eb33287dafc3ce274d039b71534048fea07bc313e0542af4e2041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355645"
---
# <a name="to-sendemailtype-element"></a>Elemento To (sendEmailType)

Contiene las direcciones de correo electrónico a las que se enviará el correo electrónico.

``` syntax
<xs:element name="To"
    type="string"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **To.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, vea [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Para el desarrollo de scripts, [**consulte EmailAction.To**](emailaction-to.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





