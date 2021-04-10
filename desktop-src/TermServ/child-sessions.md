---
title: Sesiones secundarias
description: A partir de Windows Server 2012 y Windows 8, Escritorio remoto admite el concepto de una sesión secundaria, que es una sesión especial de bucle invertido Escritorio remoto que está asociada a la sesión existente de un usuario.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268311"
---
# <a name="child-sessions"></a>Sesiones secundarias

A partir de Windows Server 2012 y Windows 8, Escritorio remoto admite el concepto de una *sesión secundaria*, que es una sesión especial de bucle invertido escritorio remoto que está asociada a la sesión existente de un usuario.

Las sesiones secundarias no se admiten en los siguientes sistemas operativos:

<dl> Windows RT  
Opción de instalación Server Core de Windows Server 2012  
Microsoft Hyper-V Server 2012  
</dl>

Un sistema solo puede tener una sesión secundaria activa y conectada en un momento dado.

La sesión secundaria se puede finalizar cerrando la sesión directamente de la misma o se terminará cuando finalice la sesión principal.

Antes de poder usar las sesiones secundarias en un sistema, debe habilitar la funcionalidad de la sesión secundaria mediante una llamada a la función [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) . También puede determinar si las sesiones secundarias se han habilitado mediante la función [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .

Una sesión secundaria solo se puede crear desde dentro de una sesión de usuario existente mediante el [escritorio remoto control ActiveX](remote-desktop-activex-control.md) y estableciendo la propiedad "ConnectToChildSession" con [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) antes de la conexión. Cuando se llama al método [**IMsTscAx. Connect**](imstscax-connect.md) , el control ActiveX escritorio remoto iniciará sesión automáticamente en la sesión secundaria sin pedir credenciales, excepto cuando el usuario haya iniciado sesión en la sesión primaria con una tarjeta inteligente. A diferencia de una sesión de Escritorio remoto normal, un usuario no necesita el derecho interactivo remoto para iniciar sesión en la sesión secundaria, ya que se trata de una sesión de bucle invertido.

No se puede bloquear una sesión secundaria. No tendrá ningún protector de pantalla ni ninguna pantalla de inicio de sesión. Además, a diferencia de una sesión normal, si se establece la Directiva de texto de inicio de sesión de WinLogon, el texto de inicio de sesión no se mostrará en esta sesión secundaria. Además, no habrá ningún efecto de Conexión a Escritorio remoto directivas de grupo de tiempo de espera en la sesión secundaria si se establecen estas directivas.

Las siguientes API se usan junto con las sesiones secundarias:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Propiedad "ConnectToChildSession" en [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)

 

 




