---
title: Sesiones secundarias
description: A partir de Windows Server 2012 y Windows 8, Escritorio remoto admite el concepto de sesión secundaria, que es una sesión de bucle Escritorio remoto especial que está asociada a la sesión existente de un usuario.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d79fa6e18cece69c672b60a65e679441ce986a6cd8a0ad46524440738c3844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010425"
---
# <a name="child-sessions"></a>Sesiones secundarias

A partir de Windows Server 2012 y Windows 8, Escritorio remoto admite el concepto de sesión secundaria *,* que es una sesión de bucle Escritorio remoto especial que está asociada a la sesión existente de un usuario.

Las sesiones secundarias no se admiten en los siguientes sistemas operativos:

<dl> Windows RT  
Windows Server 2012 Opción de instalación server core  
Microsoft Hyper-V Server 2012  
</dl>

Un sistema solo puede tener una sesión secundaria activa y conectada en un momento dado.

La sesión secundaria se puede finalizar si se cierra la sesión directamente desde ella o se finalizará cuando finalice su sesión primaria.

Para poder usar sesiones secundarias en un sistema, debe habilitar la funcionalidad de sesión secundaria mediante una llamada a la [**función WTSEnableChildSessions.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) También puede determinar si las sesiones secundarias se han habilitado mediante la [**función WTSIsChildSessionsEnabled.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)

Una sesión secundaria solo se puede crear desde dentro de la sesión de un usuario existente mediante el [control Escritorio remoto ActiveX](remote-desktop-activex-control.md) y estableciendo la propiedad "ConnectToChildSession" con [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) antes de conectarse. Cuando se llama al método [**IMsTscAx.Conectar,**](imstscax-connect.md) el control Escritorio remoto ActiveX iniciará sesión automáticamente en la sesión secundaria sin pedir credenciales, excepto cuando el usuario haya iniciado sesión en la sesión primaria mediante una tarjeta inteligente. A diferencia de Escritorio remoto sesión normal, un usuario no necesita el derecho interactivo remoto para iniciar sesión en la sesión secundaria, ya que se trata de una sesión de bucleback.

No se puede bloquear una sesión secundaria. No tendrá ningún protector de pantalla ni pantalla de inicio de sesión. Además, a diferencia de una sesión normal, si se establece la directiva de texto de inicio de sesión de WinLogon, el texto de inicio de sesión no se mostrará en esta sesión secundaria. Además, no habrá ningún efecto de las directivas Conexión a Escritorio remoto grupo de tiempo de espera en la sesión secundaria si se establecen estas directivas.

Las siguientes API se usan junto con las sesiones secundarias:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Propiedad "ConnectToChildSession" [ **en IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)

 

 




