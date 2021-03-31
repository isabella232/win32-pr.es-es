---
description: Cuando se habilitan Terminal Services, GINA debe llamar a las funciones de compatibilidad con Winlogon para completar la instalación de cada usuario, consultar las credenciales de una sesión de cliente Terminal Services y desconectarse de una sesión de red Terminal Services. Nota las dll de GINA se omiten en Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Terminal Services funciones GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907865"
---
# <a name="terminal-services-gina-functions"></a>Terminal Services funciones GINA

Cuando se habilitan Terminal Services, [*Gina*](../secgloss/g-gly.md) debe llamar a las funciones de compatibilidad con [*Winlogon*](../secgloss/w-gly.md) para completar la instalación de cada usuario, consultar las [*credenciales*](../secgloss/c-gly.md) de una sesión de cliente Terminal Services y desconectarse de una sesión de red Terminal Services.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Estas funciones de compatibilidad incluyen lo siguiente.



| Función                                                                     | Descripción                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Completa la instalación del usuario.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Se llama para consultar las credenciales de clientes remotos que no usan una licencia de conector de Internet. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Se llama para consultar las credenciales de clientes remotos que usan una licencia de conector de Internet.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Se llama para recuperar Terminal Services información de configuración de usuario.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Se llama para desconectarse de una sesión de red Terminal Services.                                      |



 

Para tener acceso a estas funciones de compatibilidad con Winlogon, el archivo DLL de GINA debe usar la estructura [**WLX \_ Dispatch \_ versión \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) . En la función [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) de Gina, ambos parámetros deben ser al menos WLX \_ versión \_ 1 \_ 3.

 

 
