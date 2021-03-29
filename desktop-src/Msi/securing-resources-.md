---
description: La capacidad del Windows Installer para establecer permisos de acceso en servicios, archivos, carpetas creadas y entradas del registro puede ayudar a que las aplicaciones de instalación sean más seguras.
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: Proteger recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415fe7b2df343a54aa0819031f4fd22b05857618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652737"
---
# <a name="securing-resources"></a>Proteger recursos

La capacidad del Windows Installer para establecer permisos de acceso en servicios, archivos, carpetas creadas y entradas del registro puede ayudar a que las aplicaciones de instalación sean más seguras. El uso de las tablas [MsiLockPermissionsEx](msilockpermissionsex-table.md) o [LockPermissions](lockpermissions-table.md) para proteger los recursos es una de las directrices recomendadas [para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md). La tabla MsiLockPermissionsEx puede permitir que el autor de un paquete proteja un recurso sin tener que escribir una [acción personalizada](custom-actions.md).

A partir de los paquetes desarrollados para Windows Installer 5,0, la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) debe reemplazar el uso de la tabla [LockPermissions](lockpermissions-table.md) . La funcionalidad extendida proporcionada por la tabla MsiLockPermissionsEx permite a un paquete proteger los [servicios](../services/services.md)de Windows, los archivos, las carpetas y las claves del registro. Un paquete no debe contener las tablas MsiLockPermissionsEx y LockPermissions.

Windows Installer 4,5 y anteriores omiten la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md). A partir de Windows Installer 5,0, se produce un error en la instalación con un mensaje de error 1941 si el paquete contiene una [tabla LockPermissions](lockpermissions-table.md) y una tabla MsiLockPermissionsEx. Los paquetes de instalación existentes que contienen solo la tabla LockPermissions se pueden instalar con Windows Installer 5,0.

Windows Installer 5,0 procesa la información de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) cuando ejecuta las acciones [InstallFiles](installfiles-action.md), [InstallServices](installservices-action.md), [WriteRegistryValues](writeregistryvalues-action.md) y [CreateFolders](createfolders-action.md) . Se debe instalar o volver a instalar un objeto protegible para protegerlo y no es posible anexar una [lista de Access Control](../secauthz/access-control-lists.md) (ACL) a un objeto existente sin tener que volver a instalar el objeto.

Para especificar el servicio, el archivo, el directorio o la clave del registro que se va a proteger, escriba la información de identificación en los campos LockObject y tabla de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) . Un objeto se identifica por su clave principal en la tabla [ServiceInstall](serviceinstall-table.md), en la tabla de [archivos](file-table.md), en la [tabla del registro](registry-table.md)o en la [tabla CreateFolder](createfolder-table.md).

Para solicitar que se apliquen los permisos especificados a un objeto, escriba una cadena de descriptor de seguridad válida en el campo *SDDLText* de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) mediante el [lenguaje de definición de descriptores de seguridad](../secauthz/security-descriptor-definition-language.md) (SDDL) válido. La tabla **MsiLockPermissionsEx** puede especificar un descriptor de seguridad que deniegue permisos, especifica la herencia de permisos de un recurso primario o especifica los permisos de una nueva cuenta. Para obtener una lista de todos los permisos que se pueden conceder, denegar o heredar, vea [cadenas ACE](../secauthz/ace-strings.md). Windows Installer 5,0 extiende el conjunto de identificadores de seguridad disponibles (SID). Para obtener una lista de los SID válidos, vea [cadenas de SID](../secauthz/sid-strings.md).

> [!NOTE]
> Si desea configurar el descriptor de seguridad de un recurso primario para especificar que los objetos secundarios heredan sus permisos, el instalador debe aplicar permisos al recurso primario antes de crear los objetos secundarios. Si el instalador crea los objetos secundarios antes de aplicar los permisos heredables al recurso primario, los permisos del recurso primario no se propagarán a los objetos secundarios.

A partir de Windows Installer 5,0, el tipo de datos [FormattedSDDLText](formattedsddltext.md) extiende el tipo de datos [con formato](formatted.md) . El Windows Installer valida que la cadena FormattedSDDLText especificada en la columna SDDLText de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) se ajuste al formato de la [cadena de descriptor de seguridad](../secauthz/security-descriptor-string-format.md).

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. La tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) y el tipo de datos [FormattedSDDLText](formattedsddltext.md) están disponibles a partir de Windows Installer 5,0.

 

 
