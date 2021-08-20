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
ms.openlocfilehash: 8aa87679c6d6db725c26deee817fe04acacca85e39d3a8f75c04cba9680ea846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132070"
---
# <a name="attachments-sendemailtype-element"></a>Elemento Attachments (sendEmailType)

Contiene una lista de datos adjuntos en el mensaje de correo electrónico.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

El tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) define el elemento **Attachments.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                          | Tipo                                                                    | Descripción                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Archivo**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, vea [**Propiedad Attachments de IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)

Para el desarrollo de scripts, [**vea EmailAction.Attachments.**](emailaction-attachments.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





