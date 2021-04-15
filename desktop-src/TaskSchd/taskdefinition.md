---
title: Objeto TaskDefinition
description: Objeto de scripting que define todos los componentes de una tarea, como la configuración de la tarea, los desencadenadores, las acciones y la información de registro.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Objeto TaskDefinition Programador de tareas
- Programador de tareas de objeto TaskDefinition, descrito
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534462"
---
# <a name="taskdefinition-object"></a>Objeto TaskDefinition

Objeto de scripting que define todos los componentes de una tarea, como la configuración de la tarea, los desencadenadores, las acciones y la información de registro.

## <a name="members"></a>Miembros

El objeto **TaskDefinition** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **TaskDefinition** tiene estas propiedades.



| Propiedad                                                               | Tipo de acceso           | Descripción                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acciones**](taskdefinition-actions.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece una colección de acciones que realiza la tarea.<br/>                                                                                                         |
| [**Data**](taskdefinition-data.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece los datos asociados a la tarea. El servicio Programador de tareas omite estos datos, pero lo usan terceros que desean ampliar el formato de la tarea.<br/> |
| [**Principal**](taskdefinition-principal.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece la entidad de seguridad de la tarea que proporciona las credenciales de seguridad para la tarea.<br/>                                                                                 |
| [**RegistrationInfo**](taskdefinition-registrationinfo.md)<br/> | Lectura/escritura<br/> | Obtiene o establece la información de registro que se utiliza para describir una tarea, como la descripción de la tarea, el autor de la tarea y la fecha en que se ha registrado la tarea.<br/> |
| [**Configuración**](taskdefinition-settings.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece la configuración que define cómo realiza la tarea el servicio de Programador de tareas.<br/>                                                                                      |
| [**Desencadenadores**](taskdefinition-triggers.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece una colección de desencadenadores que se utilizan para iniciar una tarea.<br/>                                                                                                         |
| [**XmlText**](taskdefinition-xmltext.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece la definición con formato XML de la tarea.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, se especifica una definición de tarea mediante el elemento [**Task**](taskschedulerschema-task-element.md) del esquema programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md) , ejemplo de desencadenador de [eventos (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo [de](boot-trigger-example--scripting-.md) [desencadenador de registro (](registration-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador semanal (](weekly-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de inicio de sesión](logon-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





