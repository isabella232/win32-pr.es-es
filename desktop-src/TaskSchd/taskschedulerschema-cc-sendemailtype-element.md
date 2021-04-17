---
title: Elemento CC (sendEmailType)
description: Contiene las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Elemento CC Programador de tareas
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491686"
---
# <a name="cc-sendemailtype-element"></a>Elemento CC (sendEmailType)

Contiene las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

El elemento **CC** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**propiedad CC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).

Para el desarrollo de scripts, vea [**EmailAction.CC**](emailaction-cc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





