---
title: Elemento Attachments (sendEmailType)
description: Contiene una lista de datos adjuntos en el mensaje de correo electrónico.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Elemento Attachments Programador de tareas
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803229"
---
# <a name="attachments-sendemailtype-element"></a>Elemento Attachments (sendEmailType)

Contiene una lista de datos adjuntos en el mensaje de correo electrónico.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

El elemento **Attachments** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                          | Tipo                                                                    | Descripción                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Archivo**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Para el desarrollo de scripts, vea [**EmailAction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





