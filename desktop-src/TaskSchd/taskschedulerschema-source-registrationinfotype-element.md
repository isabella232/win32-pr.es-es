---
title: Elemento Source (registrationInfoType)
description: Especifica el origen desde el que se originó la tarea. Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Elemento de origen Programador de tareas
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422031"
---
# <a name="source-registrationinfotype-element"></a>Elemento Source (registrationInfoType)

Especifica el origen desde el que se originó la tarea. Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

El elemento de **origen** se define mediante el tipo complejo de [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el origen de una tarea se especifica mediante la propiedad [**RegistrationInfo. Source**](registrationinfo-source.md) .

En el desarrollo de C++, el origen de una tarea se especifica mediante la propiedad [**IRegistrationInfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .

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

 

 





