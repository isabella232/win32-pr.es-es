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
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535488"
---
# <a name="subject-sendemailtype-element"></a>Elemento Subject (sendEmailType)

Contiene el asunto del mensaje de correo electrónico.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

El elemento de **asunto** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad Subject de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).

Para el desarrollo de scripts, vea [**EmailAction. Subject**](emailaction-subject.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





