---
title: Cc (sendEmailType) (Elemento)
description: Contiene las direcciones de correo electrónico usadas en la línea CC de un mensaje de correo electrónico.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Cc, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b639116a514a48eeab35561d936b6e5b8a4b479a9f8f0f09b6d1b596bd5e4bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334615"
---
# <a name="cc-sendemailtype-element"></a>Cc (sendEmailType) (Elemento)

Contiene las direcciones de correo electrónico usadas en la línea CC de un mensaje de correo electrónico.

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **Cc.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, vea [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).

Para el desarrollo de scripts, [**consulte EmailAction.Cc**](emailaction-cc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





