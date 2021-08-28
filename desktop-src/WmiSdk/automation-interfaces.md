---
description: Hace que las interfaces de Scripting API para WMI estén disponibles para los programadores de C/C++, en lugar de las versiones de LA API COM.
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: Automation Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c05c1682513e0c0a0d76d88990e80bcc8e6e2d22767ea6fced6f1facca59119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820295"
---
# <a name="automation-interfaces"></a>Automation Interfaces

La API de Automation hace que las interfaces de Scripting API para WMI estén disponibles para los programadores de C/C++, en lugar de las versiones de LA API COM.

En la tabla siguiente se enumeran los objetos WMI y cómo se usan en la API de Automation. Vínculo entre referencias a la documentación de la interfaz de Scripting API para equivalentes de WMI.



| Objeto automation                                 | Descripción                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**ISWbemEventSource**](swbemeventsource.md)     | Recupera eventos junto conISWbemServices.Exe [**cNotificationQuery**](swbemservices-execnotificationquery.md).   |
| [**ISWbemLastError**](swbemlasterror.md)         | Proporciona información de error extendida cuando se produce un error.                                                                   |
| [**ISWbemLocator**](swbemlocator.md)             | Obtiene una referencia a un [**objeto ISWbemServices**](swbemservices.md) que puede tener acceso a WMI en un equipo host determinado. |
| [**ISWbemMethod**](swbemmethod.md)               | Contiene una definición de método única.                                                                                        |
| [**ISWbemMethodSet**](swbemmethodset.md)         | Obtiene acceso a una colección de [**objetos ISWbemMethod.**](swbemmethod.md)                                                 |
| [**ISWbemNamedValue**](swbemnamedvalue.md)       | Contiene un único valor con nombre.                                                                                              |
| [**ISWbemNamedValueSet**](swbemnamedvalueset.md) | Obtiene acceso a una colección de [**objetos ISWbemNamedValue.**](swbemnamedvalue.md)                                         |
| [**ISWbemObject**](swbemobject.md)               | Contiene y manipula una única clase Modelo de información común objeto (CIM).                                  |
| [**ISWbemObjectPath**](swbemobjectpath.md)       | Genera y valida una ruta de acceso de objeto.                                                                                     |
| [**ISWbemObjectSet**](swbemobjectset.md)         | Obtiene acceso a una colección de [**objetos ISWbemObject.**](swbemobject.md)                                                 |
| [**ISWbemPrivilege**](swbemprivilege.md)         | Establece o borra un privilegio.                                                                                                 |
| [**ISWbemPrivilegeSet**](swbemprivilegeset.md)   | Obtiene acceso a una colección de [**objetos ISWbemPrivilege.**](swbemprivilege.md)                                           |
| [**ISWbemProperty**](swbemproperty.md)           | Se usa para contener una sola propiedad CIM.                                                                                      |
| [**ISWbemPropertySet**](swbempropertyset.md)     | Obtenga acceso a una colección de [**objetos ISWbemProperty.**](swbemproperty.md)                                              |
| [**ISWbemQualifier**](swbemqualifier.md)         | Contiene un calificador de clase única.                                                                                          |
| [**ISWbemQualifierSet**](swbemqualifierset.md)   | Obtiene acceso a una colección de [**objetos ISWbemQualifier.**](swbemqualifier.md)                                           |
| [**ISWbemSecurity**](swbemsecurity.md)           | Administra la configuración de seguridad, como El privilegio del modelo de objetos componentes (COM), AuthenticationLevel y ImpersonationLevel.      |
| [**ISWbemServices**](swbemservices.md)           | Crea, actualiza y recupera instancias o clases.                                                                       |
| [**ISWbemSink**](swbemsink.md)                   | Recibe los resultados de las operaciones asincrónicas de la aplicación cliente y las notificaciones de eventos.                                 |



 

 

 



