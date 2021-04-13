---
title: Elemento RegistrationInfo (taskType)
description: Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- información de registro Programador de tareas, elemento XML
- Programador de tareas del elemento RegistrationInfo
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491675"
---
# <a name="registrationinfo-tasktype-element"></a>Elemento RegistrationInfo (taskType)

Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

El elemento **RegistrationInfo** se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define la tarea que realiza el servicio Programador de tareas.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                  | Tipo     | Descripción                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autor (registrationInfoType)**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Especifica el autor de la tarea.<br/>                                                                              |
| [**Fecha (registrationInfoType)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Especifica la fecha y hora en que se registra la tarea.<br/>                                                       |
| [**Descripción (registrationInfoType)**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Especifica la descripción de la tarea.<br/>                                                                         |
| [**Documentación (registrationInfoType)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Especifica cualquier documentación adicional para la tarea.<br/>                                                           |
| [**SecurityDescriptor (registrationInfoType)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Especifica el descriptor de seguridad de la tarea.<br/>                                                                 |
| [**Origen (registrationInfoType)**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Especifica el origen desde el que se originó la tarea. Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.<br/> |
| [**URI (registrationInfoType)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Especifica el URI de la tarea.<br/>                                                                                 |
| [**Versión (registrationInfoType)**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Especifica el número de versión de la tarea.<br/>                                                                      |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, la información de registro de una tarea se especifica mediante la propiedad [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .

En el desarrollo de C++, la información de registro de una tarea se especifica mediante la [**propiedad RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





