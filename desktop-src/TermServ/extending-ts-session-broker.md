---
title: Extensión del Agente de sesión de Terminal Services
description: Puede extender TS \ 160; Agente de sesión mediante la interfaz COM de IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c859320c11a128ab01a719d17abd9927ea96f312e0aa3df5f0be76dcc0226b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737695"
---
# <a name="extending-terminal-services-session-broker"></a>Extensión del Agente de sesión de Terminal Services

El Agente de sesión de Terminal Services (TS Session Broker) determina si un usuario que inicia una conexión ya tiene una sesión abierta. Si es así, TS Session Broker enruta la conexión entrante al servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) con la sesión existente. Si no es así, el Agente de sesión de TS enruta la conexión entrante al servidor host de sesión de Escritorio remoto con el menor número de sesiones.

Puede extender el agente de sesión de TS mediante la [**interfaz COM de IWTSSBPlugin.**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) Puede usar esta interfaz para administrar conexiones a servidores host de sesión de Escritorio remoto, así como cualquier tipo de conexión Protocolo de escritorio remoto (RDP), por ejemplo, conexiones a máquinas virtuales invitadas que ejecutan Windows Vista Enterprise Centralized Desktop (VECD) en un host de máquina virtual de Hyper-V de Windows Server 2008.

La [**interfaz IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) ofrece varias ventajas:

-   No es necesario instalar un agente en el cliente o en el servidor host de sesión de Escritorio remoto.
-   El complemento puede interactuar sin problemas con otros servicios de rol de Servicios de Escritorio remoto, como Escritorio remoto Gateway (puerta de enlace de Escritorio remoto) y confiar en la información del Agente de sesión de TS sobre los estados de sesión y equipo.
-   Puede usar el complemento para administrar las conexiones con dispositivos cliente o servidor que admiten RDP 5.2 o posterior.
-   Puede usar el complemento para habilitar Windows Vista Enterprise centralized Desktop.

Al implementar los métodos de esta interfaz, tenga en cuenta los siguientes puntos:

-   El Agente de sesión de TS podría llamar a los métodos de este objeto COM desde varios subprocesos.
-   Si alguno de los métodos a los que se llama no se devuelve de forma inmediata y correcta, el Agente de sesión de TS no realiza más llamadas al complemento y vuelve a su lógica nativa de equilibrio de carga. Para reanudar las llamadas al complemento, debe reiniciar el servicio Agente de sesión de Terminal Services.
-   Debe registrar el complemento como un objeto COM en todo el sistema mediante Regsvr32.exe. Dado que el servicio Agente de sesión de Terminal Services se ejecuta en la cuenta "NetworkService", debe conceder a la cuenta "NetworkService" los permisos de inicio, activación y acceso necesarios mediante Dcomcnfg.exe. El servicio Agente de sesión de Terminal Services busca el CLSID del objeto COM que representa el complemento en la siguiente subclave del Registro:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** Services Extensibilidad de parámetros \\  \\ **TssdisPluginCLSID** \\  \\ 

Para obtener más información sobre Dcomcnfg.exe, vea Habilitación de la seguridad [COM mediante DCOMCNFG.](/windows/desktop/com/enabling-com-security-using-dcomcnfg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 