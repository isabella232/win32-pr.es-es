---
description: Cuando Terminal Services está habilitado, el GINA debe llamar a las funciones de soporte técnico de Winlogon para completar la configuración de cada usuario, para consultar las credenciales de una sesión de cliente de Terminal Services y para desconectarse de una sesión de red de Terminal Services. Tenga en cuenta que los archivos DLL de GINA se omiten Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Funciones GINA de Terminal Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160952"
---
# <a name="terminal-services-gina-functions"></a>Funciones GINA de Terminal Services

Cuando Terminal Services está habilitado, [*el GINA*](../secgloss/g-gly.md) debe llamar a las funciones de [](../secgloss/c-gly.md) soporte técnico de [*Winlogon*](../secgloss/w-gly.md) para completar la configuración de cada usuario, para consultar las credenciales de una sesión de cliente de Terminal Services y para desconectarse de una sesión de red de Terminal Services.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Estas funciones de compatibilidad incluyen lo siguiente.



| Función                                                                     | Descripción                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Completa la configuración del usuario.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Se llama para consultar las credenciales de los clientes remotos que no usan una licencia de conector de Internet. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Se llama para consultar las credenciales de los clientes remotos que usan una licencia de conector de Internet.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Se llama para recuperar información de configuración de usuario de Terminal Services.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Se llama para desconectarse de una sesión de red de Terminal Services.                                      |



 

Para acceder a estas funciones de compatibilidad de Winlogon, el archivo DLL de GINA debe usar la estructura [**WLX \_ DISPATCH VERSION \_ \_ 1 \_ 3.**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) En la función [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) de la GINA, ambos parámetros deben ser al menos WLX \_ VERSION \_ 1 \_ 3.

 

 
