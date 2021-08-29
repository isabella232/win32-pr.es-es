---
description: La funcionalidad del instalador de Windows para establecer permisos de acceso en servicios, archivos, carpetas creadas y entradas del Registro puede ayudar a proteger las aplicaciones de instalación.
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: Protección de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5005f906118d4f5e321b062dd4c98c9a6204d90190b60b0275f636763bcd9cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040855"
---
# <a name="securing-resources"></a>Protección de recursos

La funcionalidad del instalador de Windows para establecer permisos de acceso en servicios, archivos, carpetas creadas y entradas del Registro puede ayudar a proteger las aplicaciones de instalación. El uso de las [tablas MsiLockPermissionsEx](msilockpermissionsex-table.md) o [LockPermissions](lockpermissions-table.md) para proteger los recursos es una de las directrices recomendadas para crear [instalaciones seguras.](guidelines-for-authoring-secure-installations.md) La tabla MsiLockPermissionsEx puede permitir que un autor del paquete proteja un recurso sin tener que escribir una [acción personalizada.](custom-actions.md)

A partir de los paquetes desarrollados para Windows Installer 5.0, la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) debe reemplazar el uso de [la tabla LockPermissions.](lockpermissions-table.md) La funcionalidad extendida proporcionada por la tabla MsiLockPermissionsEx permite a un paquete proteger Windows [Services,](../services/services.md)archivos, carpetas y claves del Registro. Un paquete no debe contener las tablas MsiLockPermissionsEx y LockPermissions.

Windows El instalador 4.5 y versiones anteriores omiten [la tabla MsiLockPermissionsEx](msilockpermissionsex-table.md). A partir de Windows Installer 5.0, se produce un error en la instalación con un mensaje de error 1941 si el paquete contiene una tabla [LockPermissions](lockpermissions-table.md) y una tabla MsiLockPermissionsEx. Los paquetes de instalación existentes que contienen solo la tabla LockPermissions se pueden instalar con Windows Installer 5.0.

Windows El instalador 5.0 procesa la información de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) cuando ejecuta las acciones estándar [InstallFiles](installfiles-action.md), [InstallServices,](installservices-action.md) [WriteRegistryValues](writeregistryvalues-action.md) y [CreateFolders.](createfolders-action.md) Un objeto protegible debe instalarse o reinstalarse para protegerse y no es posible anexar una lista de Access Control (ACL) [a](../secauthz/access-control-lists.md) un objeto existente sin volver a instalar ese objeto.

Para especificar el servicio, archivo, directorio o clave del Registro que se va a proteger, escriba la información de identificación en los campos LockObject y Table de la [tabla MsiLockPermissionsEx.](msilockpermissionsex-table.md) Un objeto se identifica mediante su clave principal en [ServiceInstall Table](serviceinstall-table.md), [File Table](file-table.md), [Registry Table](registry-table.md)o [CreateFolder Table](createfolder-table.md).

Para solicitar que los permisos especificados se apliquen a un objeto, escriba una cadena de descriptor de seguridad válida en el campo *SDDLText* de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) mediante el lenguaje de definición de [descriptor](../secauthz/security-descriptor-definition-language.md) de seguridad (SDDL) válido. La **tabla MsiLockPermissionsEx** puede especificar un descriptor de seguridad que deniegue permisos, especifique la herencia de permisos de un recurso primario o especifique los permisos de una nueva cuenta. Para obtener una lista de todos los permisos que se pueden conceder, denegar o heredar, vea [Ace Strings](../secauthz/ace-strings.md). Windows Installer 5.0 amplía el conjunto de identificadores de seguridad disponibles (SID). Para obtener una lista de los SID válidos, vea [SID Strings](../secauthz/sid-strings.md).

> [!NOTE]
> Si desea configurar el descriptor de seguridad de un recurso primario para especificar que los objetos secundarios hereden sus permisos, el instalador debe aplicar permisos al recurso primario antes de crear los objetos secundarios. Si el instalador crea los objetos secundarios antes de aplicar los permisos heredables al recurso primario, los permisos del recurso primario no se propagarán a los objetos secundarios.

A partir Windows Installer 5.0, el tipo de datos [FormattedSDDLText](formattedsddltext.md) amplía el [tipo de datos Formatted.](formatted.md) El Windows de archivos valida que la cadena FormattedSDDLText especificada en la columna SDDLText de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) se ajusta al formato de cadena del descriptor de [seguridad](../secauthz/security-descriptor-string-format.md).

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. La [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) y el tipo de datos [FormattedSDDLText](formattedsddltext.md) están disponibles a partir Windows Installer 5.0.

 

 
