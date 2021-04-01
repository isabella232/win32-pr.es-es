---
title: Extender Terminal Services agente de sesiones
description: Puede extender TS \ 160; Agente de sesiones mediante la interfaz COM IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793119"
---
# <a name="extending-terminal-services-session-broker"></a>Extender Terminal Services agente de sesiones

Terminal Services agente de sesiones (agente de sesiones de TS) determina si un usuario que inicia una conexión ya tiene una sesión abierta. Si es así, el agente de sesiones de TS enruta la conexión entrante al servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) con la sesión existente. De lo contrario, el agente de sesiones de TS enruta la conexión entrante al servidor host de sesión de escritorio remoto con el menor número de sesiones.

Puede extender el agente de sesiones de TS mediante la interfaz com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) . Puede usar esta interfaz para administrar las conexiones a los servidores host de sesión de escritorio remoto, así como a cualquier tipo de conexión Protocolo de escritorio remoto (RDP), por ejemplo, las conexiones a las máquinas virtuales invitadas que ejecutan el escritorio centralizado de Windows Vista Enterprise (VECD) en un host de máquina virtual de Hyper-V de Windows Server 2008.

La interfaz [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) ofrece varias ventajas:

-   No es necesario instalar un agente en el cliente o en el servidor host de sesión de escritorio remoto.
-   El complemento puede interactuar sin problemas con otros servicios de rol de Servicios de Escritorio remoto, como Escritorio remoto puerta de enlace de RD, y basarse en la información del agente de sesiones de TS sobre los Estados de sesión y equipo.
-   Puede usar el complemento para administrar conexiones con dispositivos cliente o servidor que admitan RDP 5,2 o posterior.
-   Puede usar el complemento para habilitar las soluciones de escritorio centralizadas de Windows Vista Enterprise.

Cuando implemente los métodos de esta interfaz, tenga en cuenta los puntos siguientes:

-   El agente de sesiones de TS podría llamar a los métodos de este objeto COM desde varios subprocesos.
-   Si alguno de los métodos a los que se llama no vuelve inmediatamente y correctamente, el agente de sesiones de TS no realiza más llamadas al complemento y revierte a su lógica de equilibrio de carga nativa. Para reanudar las llamadas al complemento, debe reiniciar el servicio agente de sesiones de Terminal Services.
-   Debe registrar el complemento como un objeto COM en todo el sistema mediante Regsvr32.exe. Dado que el servicio agente de sesiones de Terminal Services se ejecuta bajo la cuenta "NetworkService", debe proporcionar a la cuenta "NetworkService" los permisos de inicio, activación y acceso necesarios mediante Dcomcnfg.exe. El servicio agente de sesiones de Terminal Services busca el CLSID del objeto COM que representa el complemento en la subclave del Registro siguiente:

    **HKEY \_ \_** Parámetros de Tssdis de sistema de equipo local de \\  \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **ExtensibilityPluginCLSID**

Para obtener más información acerca de Dcomcnfg.exe, vea [Habilitar la seguridad de com mediante DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 