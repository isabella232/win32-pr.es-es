---
description: Hace que las interfaces de la API de scripting para WMI estén disponibles para los programadores de C/C++, en lugar de las versiones de la API de COM.
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: Interfaces de automatización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652e9a1fb35a66bddb9f0aebe543770e89e6e2ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706936"
---
# <a name="automation-interfaces"></a>Interfaces de automatización

La API de automatización hace que las interfaces de la API de scripting para WMI estén disponibles para los programadores de C/C++, en lugar de las versiones de la API de COM.

En la tabla siguiente se enumeran los objetos WMI y cómo se utilizan en la API de automatización. El vínculo referencias cruzadas a la documentación de la interfaz para la API de scripting para los equivalentes de WMI.



| Objeto Automation                                 | Descripción                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**ISWbemEventSource**](swbemeventsource.md)     | Recupera eventos junto con [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).   |
| [**ISWbemLastError**](swbemlasterror.md)         | Proporciona información de error extendida cuando se produce un error.                                                                   |
| [**ISWbemLocator**](swbemlocator.md)             | Obtiene una referencia a un objeto [**ISWbemServices**](swbemservices.md) que puede tener acceso a WMI en un equipo host determinado. |
| [**ISWbemMethod**](swbemmethod.md)               | Contiene una definición de método único.                                                                                        |
| [**ISWbemMethodSet**](swbemmethodset.md)         | Obtiene acceso a una colección de objetos [**ISWbemMethod**](swbemmethod.md) .                                                 |
| [**ISWbemNamedValue**](swbemnamedvalue.md)       | Contiene un solo valor con nombre.                                                                                              |
| [**ISWbemNamedValueSet**](swbemnamedvalueset.md) | Obtiene acceso a una colección de objetos [**ISWbemNamedValue**](swbemnamedvalue.md) .                                         |
| [**ISWbemObject**](swbemobject.md)               | Contiene y manipula una única clase o instancia de objeto de Modelo de información común (CIM).                                  |
| [**ISWbemObjectPath**](swbemobjectpath.md)       | Genera y valida una ruta de acceso del objeto.                                                                                     |
| [**ISWbemObjectSet**](swbemobjectset.md)         | Obtiene acceso a una colección de objetos [**ISWbemObject**](swbemobject.md) .                                                 |
| [**ISWbemPrivilege**](swbemprivilege.md)         | Establece o borra un privilegio.                                                                                                 |
| [**ISWbemPrivilegeSet**](swbemprivilegeset.md)   | Obtiene acceso a una colección de objetos [**ISWbemPrivilege**](swbemprivilege.md) .                                           |
| [**ISWbemProperty**](swbemproperty.md)           | Se usa para contener una única propiedad CIM.                                                                                      |
| [**ISWbemPropertySet**](swbempropertyset.md)     | Obtiene acceso a una colección de objetos [**ISWbemProperty**](swbemproperty.md) .                                              |
| [**ISWbemQualifier**](swbemqualifier.md)         | Contiene un calificador de una sola clase.                                                                                          |
| [**ISWbemQualifierSet**](swbemqualifierset.md)   | Obtiene acceso a una colección de objetos [**ISWbemQualifier**](swbemqualifier.md) .                                           |
| [**ISWbemSecurity**](swbemsecurity.md)           | Administra la configuración de seguridad, como el privilegio del modelo de objetos componentes (COM), AuthenticationLevel e ImpersonationLevel.      |
| [**ISWbemServices**](swbemservices.md)           | Crea, actualiza y recupera instancias o clases.                                                                       |
| [**ISWbemSink**](swbemsink.md)                   | Recibe los resultados de las operaciones asincrónicas y las notificaciones de eventos de la aplicación cliente.                                 |



 

 

 



