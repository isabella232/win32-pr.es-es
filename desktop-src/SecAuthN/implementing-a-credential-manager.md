---
description: Muestra las exportaciones de DLL que se deben implementar para crear un administrador de credenciales.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementación de un administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912481"
---
# <a name="implementing-a-credential-manager"></a>Implementación de un administrador de credenciales

Para crear un administrador de credenciales, debe crear un archivo DLL que exporte las siguientes funciones:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Para restaurar las notificaciones a las funciones [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) y [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) para el inicio de sesión con tarjeta inteligente, cree una entrada del registro denominada **SmartCardLogonNotify** como **DWORD** y establézcala en 1:

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

**Windows Server 2003 y Windows XP:** La entrada del registro **SmartCardLogonNotify** no es necesaria.

Además, los administradores de credenciales también deben admitir la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para WNNC \_ Start (no es necesario admitir otros índices para los administradores de credenciales). Esto indica a MPR Cuándo se iniciará un administrador de credenciales. Al llamar a **NPGetCaps** con el parámetro *NINDEX* establecido en WNNC \_ Start, el MPR obtiene el tiempo de espera antes de llamar a las funciones de punto de entrada de administración de credenciales del proveedor. Y si el MPR tiene esta información, puede reenviarla al administrador de credenciales y establecer el tiempo de espera.

 

 



