---
title: Devoluciones de llamada de combinación local
description: Una vez que IGMP notifica al administrador del grupo de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de \_ devolución de llamada de combinación local de PMGM \_ \_ al Protocolo de enrutamiento que posee la interfaz si existe una.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486938"
---
# <a name="local-join-callbacks"></a>Devoluciones de llamada de combinación local

Una vez que IGMP notifica al administrador del grupo de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de [**\_ devolución de \_ \_ llamada de combinación local de PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) al Protocolo de enrutamiento que posee la interfaz si existe una. Esta devolución de llamada notifica al Protocolo de enrutamiento el cambio.

Esta devolución de llamada y la devolución de llamada de [**\_ \_ salida \_ local de PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) se usan para sincronizar el reenvío entre IGMP y los protocolos de enrutamiento.

 

 




