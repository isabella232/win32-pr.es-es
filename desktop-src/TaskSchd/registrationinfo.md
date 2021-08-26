---
title: Objeto RegistrationInfo
description: Objeto de scripting que proporciona la información administrativa que se puede usar para describir la tarea.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- información de registro Programador de tareas , objeto
- Registro de objetos RegistrationInfo Programador de tareas
- Objeto RegistrationInfo Programador de tareas , descrito
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85bb423ae27a3d0b0b15f7b04d287a749f4fe23f3a4b58f7c2462b487b8a705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072655"
---
# <a name="registrationinfo-object"></a>Objeto RegistrationInfo

Objeto de scripting que proporciona la información administrativa que se puede usar para describir la tarea. Esta información incluye detalles como una descripción de la tarea, el autor de la tarea, la fecha en que se registra la tarea y el descriptor de seguridad de la tarea.

## <a name="members"></a>Miembros

El **objeto RegistrationInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto RegistrationInfo** tiene estas propiedades.



| Propiedad                                                                     | Tipo de acceso           | Descripción                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autor**](registrationinfo-author.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece el autor de la tarea.<br/>                                                                                            |
| [**Date**](registrationinfo-date.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece la fecha y hora en que se registra la tarea.<br/>                                                                     |
| [**Descripción**](registrationinfo-description.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece la descripción de la tarea.<br/>                                                                                       |
| [**Documentación**](registrationinfo-documentation.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece cualquier documentación adicional para la tarea.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Obtiene o establece el descriptor de seguridad de la tarea.<br/>                                                                               |
| [**Origen**](registrationinfo-source.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece de dónde se originó la tarea. Por ejemplo, una tarea puede originarse en un componente, servicio, aplicación o usuario.<br/> |
| [**Identificador URI**](registrationinfo-uri.md)<br/>                               | Lectura/escritura<br/> | Obtiene o establece el URI de la tarea.<br/>                                                                                               |
| [**Versión**](registrationinfo-version.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece el número de versión de la tarea.<br/>                                                                                    |
| [**Xmltext**](registrationinfo-xmltext.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece una versión con formato XML de la información de registro de la tarea.<br/>                                             |



 

## <a name="remarks"></a>Comentarios

La información de registro se puede usar para identificar una tarea a través de la interfaz Programador de tareas usuario o como criterios de búsqueda al enumerar las tareas registradas.

Al leer o escribir XML para una tarea, la información de registro de la tarea se especifica en el [**elemento RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) del Programador de tareas esquema.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





