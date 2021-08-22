---
title: Elemento Bcc (sendEmailType)
description: Contiene las direcciones de correo electrónico usadas en la línea CCO de un mensaje de correo electrónico.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Bcc element Programador de tareas
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1409d50a0317758534724b9e2c3a9796c4dd0cb40e666f58fc65ca0771da9762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659045"
---
# <a name="bcc-sendemailtype-element"></a>Elemento Bcc (sendEmailType)

Contiene las direcciones de correo electrónico usadas en la línea CCO de un mensaje de correo electrónico.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **Bcc.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Para el desarrollo de scripts, [**vea EmailAction.Bcc**](emailaction-bcc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





