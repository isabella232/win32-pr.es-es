---
description: Puede usar Win32 \_ Process. Create para ejecutar un script o una aplicación en un equipo remoto. Sin embargo, por motivos de seguridad, el proceso no puede ser interactivo. Cuando \_ se llama a Win32 Process. Create en el equipo local, el proceso puede ser interactivo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Crear procesos de forma remota mediante WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816686"
---
# <a name="creating-processes-remotely-using-wmi"></a>Crear procesos de forma remota mediante WMI

Puede usar [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) para ejecutar un script o una aplicación en un equipo remoto. Sin embargo, por motivos de seguridad, el proceso no puede ser interactivo. Cuando se llama a **Win32 \_ Process. Create** en el equipo local, el proceso puede ser interactivo.

> [!WARNING]
> En este tema se describe el procedimiento general para crear un proceso remoto con WMI. Si simplemente desea ejecutar un script en un sistema remoto, consulte [conexión a WMI de forma remota a partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)o [conexión a WMI en un equipo remoto mediante Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Para obtener más información general sobre la comunicación remota con PowerShell, vea [ejecutar comandos remotos](https://technet.microsoft.com/library/dd819505.aspx).

 

El proceso remoto no tiene ninguna interfaz de usuario, pero aparece en el **Administrador de tareas**. Un proceso creado localmente puede ejecutarse en cualquier cuenta si la cuenta tiene el permiso **Ejecutar método** para el \\ espacio de nombres root cimv2. Un proceso creado de forma remota puede ejecutarse en cualquier cuenta si la cuenta tiene los permisos **Ejecutar método** y acceso **remoto habilitado** para la raíz \\ cimv2. Los permisos **método Execute** y **Habilitar remoto** se establecen en control WMI en el panel de control. Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

Puede usar [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) para crear un proceso interactivo de forma remota. Pero los procesos iniciados por **Win32 \_ ScheduledJob. Create** se ejecutan en la cuenta LocalSystem que puede conferir demasiados privilegios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Conexión a un tercer equipo: Delegación](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
