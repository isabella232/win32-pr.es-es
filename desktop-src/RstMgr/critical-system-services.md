---
title: Servicios críticos del sistema
description: El administrador de reinicio no puede detener y reiniciar los servicios críticos del sistema sin necesidad de reiniciar el sistema. Las actualizaciones de cualquier archivo o recurso en uso por uno de estos servicios requieren un reinicio del sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076415"
---
# <a name="critical-system-services"></a>Servicios críticos del sistema

El administrador de reinicio no puede detener y reiniciar los servicios críticos del sistema sin necesidad de reiniciar el sistema. Las actualizaciones de cualquier archivo o recurso en uso por uno de estos servicios requieren un reinicio del sistema.

**Para determinar si un proceso es un servicio de sistema crítico.**

1.  Registre el proceso mediante la función [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .
2.  Llame a la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obtener la estructura de [**información del \_ proceso \_ de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .
3.  El miembro **ApplicationType** de la estructura [**de \_ \_ información de proceso de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) devuelta contiene un valor de enumeración de [**\_ \_ tipo de aplicación de RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) . Este valor se establece en **RmCriticial** para un proceso crítico del sistema.

Los servicios críticos del sistema incluyen smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, sistema, svchost.exe con RPCSS y svchost.exe con DCOM/PnP.

 

 




