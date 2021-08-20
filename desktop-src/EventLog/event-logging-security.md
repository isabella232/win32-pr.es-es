---
description: El registro de seguridad está diseñado para su uso por el sistema. Sin embargo, los usuarios pueden leer y borrar el registro de seguridad si se les ha concedido el privilegio SE SECURITY NAME (el &0034; administrar la auditoría y el registro de \_ \_ seguridad&\# \# 0034; derecho de usuario). Para obtener más información, vea Privilegios.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Seguridad del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52f6c801b061290ebb4d6f47fe78efebc09e1b2d23dc4a598dc9f97c1b3a46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151555"
---
# <a name="event-logging-security"></a>Seguridad del registro de eventos

El **registro** de seguridad está diseñado para su uso por el sistema. Sin embargo, los usuarios  pueden leer y borrar el registro de seguridad si se les ha concedido el privilegio SE SECURITY NAME (el derecho de usuario "administrar el registro de seguridad y \_ \_ auditoría"). Para obtener más información, vea [Privileges](/windows/desktop/SecAuthZ/privileges).

Solo la autoridad de seguridad local (Lsass.exe) tiene permiso de escritura para el **registro de** seguridad. Ninguna otra cuenta puede solicitar este privilegio. Para escribir un evento en el registro **de** seguridad, use la [**función AuthzReportSecurityEvent.**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent)

El acceso al **registro de** aplicación, al **registro del** sistema y a los registros personalizados está restringido. El sistema concede acceso en función de los derechos de acceso concedidos a la cuenta en la que se ejecuta el subproceso. En la tabla siguiente se muestran los tipos de acceso que requieren las funciones de registro de eventos.



| Derecho de acceso                 | Descripción                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| ELF \_ LOGFILE \_ CLEAR (0x0004) | Requerido por [**ClearEventLog.**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                    |
| ELF \_ LOGFILE \_ READ (0x0001)  | Requerido por [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) y [**OpenEventLog.**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) |
| ESCRITURA DE ARCHIVOS DE REGISTRO DE \_ \_ ELF (0x0002) | Requerido por [**RegisterEventSource.**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)                                        |



 

Use el **valor del Registro CustomSD** para configurar la seguridad del registro de **aplicación,** el registro **del** sistema y los registros personalizados. Para obtener más información, vea [Eventlog Key](eventlog-key.md).

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



 

Para conceder acceso a los miembros de la cuenta de invitado, cambie el siguiente valor del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **EventLog** \\ *Log* \\ **RestrictGuestAccess**

 

 
