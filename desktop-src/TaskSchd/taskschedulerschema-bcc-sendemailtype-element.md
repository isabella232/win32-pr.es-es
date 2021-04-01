---
title: BCC (sendEmailType), elemento
description: Contiene las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Elemento BCC Programador de tareas
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150509"
---
# <a name="bcc-sendemailtype-element"></a>BCC (sendEmailType), elemento

Contiene las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

El elemento **BCC** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad BCC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Para el desarrollo de scripts, vea [**EmailAction. BCC**](emailaction-bcc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





