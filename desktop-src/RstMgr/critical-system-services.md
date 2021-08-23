---
title: Servicios críticos del sistema
description: El Administrador de reinicio no puede detener ni reiniciar los servicios críticos del sistema sin un reinicio del sistema. Las actualizaciones de cualquier archivo o recurso que use uno de estos servicios requieren un reinicio del sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8a50eca43a62d24e0ab6363844bef7457aaf05b34251f5d804dacabaead5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010242"
---
# <a name="critical-system-services"></a>Servicios críticos del sistema

El Administrador de reinicio no puede detener ni reiniciar los servicios críticos del sistema sin un reinicio del sistema. Las actualizaciones de cualquier archivo o recurso que use uno de estos servicios requieren un reinicio del sistema.

**Para determinar si un proceso es un servicio crítico del sistema.**

1.  Registre el proceso mediante la [**función RmRegisterResources.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources)
2.  Llame a [**la función RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obtener la [**estructura RM PROCESS \_ \_ INFO.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info)
3.  El **miembro ApplicationType** de la estructura [**RM PROCESS INFO \_ \_ devuelta**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) contiene un [**valor de enumeración RM APP \_ \_ TYPE.**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) Este valor se establece en **RmCriticial para** un proceso crítico del sistema.

Los servicios críticos del sistema incluyen smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe con RPCSS y svchost.exe con Dcom/PnP.

 

 




