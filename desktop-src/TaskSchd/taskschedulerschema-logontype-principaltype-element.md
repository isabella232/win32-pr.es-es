---
title: Elemento LogonType (principalType)
description: Especifica el método de inicio de sesión de seguridad necesario para ejecutar esas tareas asociadas a la entidad de seguridad.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Elemento LogonType Programador de tareas
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9121179b744857d5e7d0bec5a2ae814c603c6b1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259180"
---
# <a name="logontype-principaltype-element"></a>Elemento LogonType (principalType)

Especifica el método de inicio de sesión de seguridad necesario para ejecutar esas tareas asociadas a la entidad de seguridad.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

El **elemento LogonType** se define mediante el [**tipo complejo principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

El **elemento LogonType** y el [**elemento UserId**](taskschedulerschema-userid-principaltype-element.md) se usan juntos para definir el usuario necesario para ejecutar las tareas que usan esta entidad de seguridad.

Para el desarrollo de scripting, la propiedad [**Principal.LogonType**](principal-logontype.md) especifica el tipo de inicio de sesión de la entidad de seguridad.

Para el desarrollo de C++, la propiedad [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) especifica el tipo de inicio de sesión de la entidad de seguridad.

Este elemento (definido por el tipo simple [**logonType)**](taskschedulerschema-logontype-simpletype.md) debe tener uno de los siguientes valores.

-   S4U: el usuario debe iniciar sesión con un servicio para el inicio de sesión de usuario (S4U). Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no hay acceso a la red ni a los archivos cifrados.
-   Contraseña: el usuario debe iniciar sesión con una contraseña.
-   InteractiveToken: el usuario ya debe haber iniciado sesión. La tarea solo se ejecutará en una sesión interactiva existente.

Para una tarea, que contiene una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo. Para establecer que el tipo de inicio de sesión de tarea sea interactivo, especifique **InteractiveToken** en el **&lt; elemento LogonType &gt;** de la entidad de seguridad de tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





