---
description: Enumera las exportaciones dll que se deben implementar para crear un administrador de credenciales.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementación de un Administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a1787fcf72d88ad809f904f9f83179ac86631b83a23314f9d24ee31ce3dec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482665"
---
# <a name="implementing-a-credential-manager"></a>Implementación de un Administrador de credenciales

Para crear un administrador de credenciales, debe crear un archivo DLL que exporte las funciones siguientes:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Para restaurar las notificaciones a las funciones [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) y [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) para el inicio de sesión con tarjeta inteligente, cree una entrada del Registro denominada **SmartCardLogonNotify** como **DWORD** y estapórela en 1:

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

**Windows Server 2003 y Windows XP:** No se requiere la entrada del Registro **SmartCardLogonNotify.**

Además, los administradores de credenciales también deben admitir la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para WNNC START (no es necesario admitir otros índices para los administradores \_ de credenciales). Esto indica a MPR cuándo se iniciará un administrador de credenciales. Al llamar **a NPGetCaps** con el parámetro *nIndex* establecido en WNNC START, el MPR obtiene el tiempo de espera antes de llamar a las funciones de punto de entrada de administración de credenciales del \_ proveedor. Y si el MPR tiene esta información, puede reenviarla al administrador de credenciales, estableciendo el tiempo de espera.

 

 



