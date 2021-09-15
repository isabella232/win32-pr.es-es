---
description: La referencia de Scripting API para WMI describe cada objeto de scripting mediante una sintaxis específica. Para obtener una explicación de esta sintaxis, consulte Convenciones de documento para scripting API.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Objetos de API de scripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465444"
---
# <a name="scripting-api-objects"></a>Objetos de API de scripting

La referencia de Scripting API para WMI describe cada objeto de scripting mediante una sintaxis específica. Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

En la tabla siguiente se enumeran los objetos de scripting wmi y cómo se usan.



| Object                                               | Descripción                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Construye y analiza los valores [datetime de](date-and-time-format.md) CIM.                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Recupera eventos junto con [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Proporciona información de error extendida cuando se produce un error.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Obtiene un [**objeto SWbemServices**](swbemservices.md) que puede obtener acceso a WMI en un equipo host determinado.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Contiene una única definición de método WMI.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Obtiene una colección de [**objetos SWbemMethod.**](swbemmethod.md)                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Contiene un único valor con nombre.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Obtiene acceso a una colección de [**objetos SWbemNamedValue.**](swbemnamedvalue.md)                                                                                                                                                                     |
| [**SWbemObject**](swbemobject.md)                   | Contiene y manipula una única clase o instancia de objeto WMI.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Extiende la funcionalidad de [**SWbemObject.**](swbemobject.md) Este objeto agrega el [**método Refresh**](swbemrefresher-refresh.md) para [**objetos SWbemRefresher.**](swbemrefresher.md)                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Genera y valida una ruta de acceso de objeto.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Obtiene acceso a una colección de [**objetos SWbemObject.**](swbemobject.md)                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Establece o borra un privilegio.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Obtiene acceso a una colección de [**objetos SWbemPrivilege.**](swbemprivilege.md)                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Contiene una sola propiedad WMI.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Obtiene acceso a una colección de [**objetos SWbemProperty.**](swbemproperty.md)                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | Contiene un calificador de propiedad única.                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | Obtiene acceso a una colección de [**objetos SWbemQualifier.**](swbemqualifier.md)                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Recopila y actualiza los valores de propiedad del objeto en una operación.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Representa un único elemento actualizable en [**un objeto SWbemRefresher,**](swbemrefresher.md) como una propiedad .                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Administra la configuración de seguridad, como los [**privilegios**](swbemsecurity-privileges.md)del modelo de objetos componentes (COM), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)y [**ImpersonationLevel.**](swbemsecurity-impersonationlevel.md)   |
| [**SWbemServices**](swbemservices.md)               | Crea, actualiza y recupera instancias o clases.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Extiende la funcionalidad de [**SWbemServices.**](swbemservices.md) Este objeto agrega los [**métodos Put**](swbemservicesex-put.md) [**y PutAsync**](swbemservicesex-putasync.md) para permitir que una clase o instancia se guarde en varios espacios de nombres. |
| [**SWbemSink**](swbemsink.md)                       | Recibe los resultados de las operaciones asincrónicas y las notificaciones de eventos, que las aplicaciones cliente usan.                                                                                                                                        |



 

 

 



