---
title: Elemento from (sendEmailType)
description: Contiene la dirección de correo electrónico del remitente de correo electrónico.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Del elemento Programador de tareas
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079158"
---
# <a name="from-sendemailtype-element"></a>Elemento from (sendEmailType)

Contiene la dirección de correo electrónico del remitente de correo electrónico.

``` syntax
<xs:element name="From"
    type="string"
 />
```

El elemento **from** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**from (propiedad de IEmailAction)**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).

Para el desarrollo de scripts, vea [**EmailAction. from**](emailaction-from.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





