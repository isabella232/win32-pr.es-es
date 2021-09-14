---
title: Elemento File (attachmentsType)
description: Contiene la ruta de acceso a un archivo enviado como datos adjuntos en un mensaje de correo electrónico.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Archivo, elemento Programador de tareas
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259351"
---
# <a name="file-attachmentstype-element"></a>Elemento File (attachmentsType)

Contiene la ruta de acceso a un archivo enviado como datos adjuntos en un mensaje de correo electrónico.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

El **elemento File** se define mediante el tipo complejo [**attachmentsType.**](taskschedulerschema-attachmentstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                      | Derivado de                                                               | Descripción                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Datos adjuntos (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Contiene una lista de datos adjuntos en el mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**Propiedad Attachments de IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)

Para el desarrollo de scripts, [**vea EmailAction.Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





