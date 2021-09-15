---
description: Puede usar Win32 \_ Process.Create para ejecutar un script o una aplicación en un equipo remoto. Sin embargo, por motivos de seguridad, el proceso no puede ser interactivo. Cuando se llama \_ a Win32 Process.Create en el equipo local, el proceso puede ser interactivo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Crear procesos de forma remota mediante WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575384"
---
# <a name="creating-processes-remotely-using-wmi"></a>Crear procesos de forma remota mediante WMI

Puede usar [**Win32 \_ Process.Create para**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) ejecutar un script o una aplicación en un equipo remoto. Sin embargo, por motivos de seguridad, el proceso no puede ser interactivo. Cuando **se llama a Win32 \_ Process.Create** en el equipo local, el proceso puede ser interactivo.

> [!WARNING]
> En este tema se describe el procedimiento general para crear un proceso remoto con WMI. Si simplemente desea ejecutar un script en un sistema remoto, vea Conectarse a WMI de forma remota a partir de [Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)o Conectarse a WMI en un equipo remoto mediante [Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Para obtener más información general sobre la comunicación remota con PowerShell, vea [Ejecutar comandos remotos.](https://technet.microsoft.com/library/dd819505.aspx)

 

El proceso remoto no tiene ninguna interfaz de usuario, pero se muestra en la **Administrador de tareas**. Un proceso creado localmente puede ejecutarse en cualquier cuenta si la cuenta tiene el permiso **Execute Method** para el espacio de nombres \\ raíz cimv2. Un proceso creado de forma remota se puede ejecutar en cualquier cuenta si la cuenta tiene los permisos **Execute Method** y **Remote Enable** para la \\ raíz cimv2. Los **permisos Execute Method** y Remote **Enable** se establecen en el control WMI en el Panel de control. Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).

Puede usar [**\_ ScheduledJob.Create de Win32 para**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) crear un proceso interactivo de forma remota. Pero los procesos iniciados **por Win32 \_ ScheduledJob.Create** se ejecutan en la cuenta LocalSystem que puede conferir demasiados privilegios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Conexión a una tercera delegación de equipos](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
