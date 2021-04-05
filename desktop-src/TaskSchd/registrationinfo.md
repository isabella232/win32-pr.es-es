---
title: Objeto RegistrationInfo
description: Objeto de scripting que proporciona la información administrativa que se puede utilizar para describir la tarea.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- Programador de tareas de información de registro, objeto
- Objeto RegistrationInfo Programador de tareas
- Programador de tareas de objeto RegistrationInfo, descrito
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
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079102"
---
# <a name="registrationinfo-object"></a>Objeto RegistrationInfo

Objeto de scripting que proporciona la información administrativa que se puede utilizar para describir la tarea. Esta información incluye detalles como, por ejemplo, una descripción de la tarea, el autor de la tarea, la fecha de registro de la tarea y el descriptor de seguridad de la tarea.

## <a name="members"></a>Miembros

El objeto **RegistrationInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **RegistrationInfo** tiene estas propiedades.



| Propiedad                                                                     | Tipo de acceso           | Descripción                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autor**](registrationinfo-author.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece el autor de la tarea.<br/>                                                                                            |
| [**Date**](registrationinfo-date.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece la fecha y hora en que se registra la tarea.<br/>                                                                     |
| [**Descripción**](registrationinfo-description.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece la descripción de la tarea.<br/>                                                                                       |
| [**Documentación**](registrationinfo-documentation.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece cualquier documentación adicional para la tarea.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Obtiene o establece el descriptor de seguridad de la tarea.<br/>                                                                               |
| [**Origen**](registrationinfo-source.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece la ubicación de la que se originó la tarea. Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Lectura/escritura<br/> | Obtiene o establece el URI de la tarea.<br/>                                                                                               |
| [**Versión**](registrationinfo-version.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece el número de versión de la tarea.<br/>                                                                                    |
| [**XmlText**](registrationinfo-xmltext.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece una versión con formato XML de la información de registro de la tarea.<br/>                                             |



 

## <a name="remarks"></a>Observaciones

La información de registro se puede utilizar para identificar una tarea a través de la interfaz de usuario de Programador de tareas o como criterio de búsqueda al enumerar las tareas registradas.

Al leer o escribir XML para una tarea, se especifica la información de registro de la tarea en el elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





