---
title: Elemento File (attachmentsType)
description: Contiene la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Programador de tareas de elemento de archivo
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422165"
---
# <a name="file-attachmentstype-element"></a>Elemento File (attachmentsType)

Contiene la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

El elemento de **archivo** se define mediante el tipo complejo de [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                      | Derivado de                                                               | Descripción                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Datos adjuntos (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Contiene una lista de datos adjuntos en el mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Para el desarrollo de scripts, vea [**EmailAction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





