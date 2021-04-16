---
title: Elemento LogonType (principalType)
description: Especifica el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Programador de tareas del elemento LogonType
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685908"
---
# <a name="logontype-principaltype-element"></a>Elemento LogonType (principalType)

Especifica el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

El elemento **LogonType** se define mediante el tipo complejo de [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Los elementos **LogonType** y [**userid**](taskschedulerschema-userid-principaltype-element.md) se usan juntos para definir el usuario necesario para ejecutar las tareas que usan esta entidad de seguridad.

Para el desarrollo de scripting, el tipo de inicio de sesión de la entidad de seguridad se especifica mediante la propiedad [**principal. LogonType**](principal-logontype.md) .

En el desarrollo de C++, el tipo de inicio de sesión de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal:: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .

Este elemento (definido por el tipo simple [**logonType**](taskschedulerschema-logontype-simpletype.md) ) debe tener uno de los valores siguientes.

-   S4U: el usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U). Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no se tiene acceso a la red ni a los archivos cifrados.
-   Contraseña: el usuario debe iniciar sesión con una contraseña.
-   InteractiveToken: el usuario ya debe haber iniciado sesión. La tarea se ejecutará solo en una sesión interactiva existente.

En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer que el tipo de inicio de sesión de tarea sea interactivo, especifique **InteractiveToken** en el **<LogonType>** elemento de la entidad de seguridad de la tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





