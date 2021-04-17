---
description: El registro de seguridad está diseñado para su uso por parte del sistema. Sin embargo, los usuarios pueden leer y borrar el registro de seguridad si se les ha concedido el privilegio de nombre de seguridad de SE \_ \_ (el &\# 0034; administrar el registro de auditoría y de seguridad&\# 0034; derecho de usuario). Para obtener más información, vea privilegios.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Seguridad del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4e2dce7318efeb6f26917bca1d6812eb32a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687378"
---
# <a name="event-logging-security"></a>Seguridad del registro de eventos

El registro de **seguridad** está diseñado para su uso por parte del sistema. Sin embargo, los usuarios pueden leer y borrar el registro de **seguridad** si se les ha concedido el privilegio de nombre de seguridad de se \_ \_ (el derecho de usuario "Administrar registro de auditoría y de seguridad"). Para obtener más información, vea [privilegios](/windows/desktop/SecAuthZ/privileges).

Solo la autoridad de seguridad local (Lsass.exe) tiene permiso de escritura para el registro de **seguridad** . Ninguna otra cuenta puede solicitar este privilegio. Para escribir un evento en el registro de **seguridad** , utilice la función [**AuthzReportSecurityEvent**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent) .

Se restringe el acceso al registro de la **aplicación** , al registro **del sistema** y a los registros personalizados. El sistema concede acceso en función de los derechos de acceso concedidos a la cuenta en la que se ejecuta el subproceso. En la tabla siguiente se muestran los tipos de acceso que requieren las funciones de registro de eventos.



| Derecho de acceso                 | Descripción                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Archivo de registro de ELF \_ \_ Clear (0x0004) | Requerido por [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga).                                                    |
| Archivo de registro de ELF \_ \_ Read (0x0001)  | Requerido por [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) y [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga). |
| Escritura de archivo de registro de ELF \_ \_ (0x0002) | Requerido por [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea).                                        |



 

Use el **valor del registro** con protección para configurar la seguridad del registro de la **aplicación** , el registro **del sistema** y los registros personalizados. Para obtener más información, vea [EventLog Key](eventlog-key.md).

**Windows XP/2000:** En la tabla siguiente se describen los derechos de acceso concedidos para cada cuenta en cada registro.

| Log             | Cuenta                 | Lectura | Escritura | Borrar |
|-----------------|-------------------------|------|-------|-------|
| **Aplicación** | Administradores (sistema) | X    | X     | X     |
|                 | Administradores (dominio) | X    | X     | X     |
|                 | LocalSystem (Sistema local)             | X    | X     | X     |
|                 | Usuario interactivo        | X    | X     |       |
| **Sistema**      | Administradores (sistema) | X    | X     | X     |
|                 | Administradores (dominio) | X    |       | X     |
|                 | LocalSystem (Sistema local)             | X    | X     | X     |
|                 | Usuario interactivo        | X    |       |       |
| *Personalizada*        | Administradores (sistema) | X    | X     | X     |
|                 | Administradores (dominio) | X    | X     | X     |
|                 | LocalSystem (Sistema local)             | X    | X     | X     |
|                 | Usuario interactivo        | X    | X     |       |



 

Para conceder acceso a los miembros de la cuenta de invitado, cambie el siguiente valor del registro:

**HKEY \_ \_** \\ Registro de eventos **del sistema del** equipo local \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **RestrictGuestAccess**

 

 
