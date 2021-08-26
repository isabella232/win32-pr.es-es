---
title: Devoluciones de llamada de combinación local
description: Después de que IGMP notifique al administrador de grupos de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador de grupo de multidifusión invoca la devolución de llamada PMGM LOCAL JOIN CALLBACK al protocolo de enrutamiento que posee la interfaz si existe \_ \_ \_ alguna.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b3464aa645a6ab110acef09f238ffca97f781a38cc6c2602a39e7c66316490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074075"
---
# <a name="local-join-callbacks"></a>Devoluciones de llamada de combinación local

Después de que IGMP notifique al administrador de grupos de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador de grupo de multidifusión invoca la devolución de llamada [**PMGM \_ LOCAL JOIN \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) al protocolo de enrutamiento que posee la interfaz si existe alguna. Esta devolución de llamada notifica el cambio al protocolo de enrutamiento.

Esta devolución de llamada y la devolución de llamada [**\_ PMGM LOCAL \_ LEAVE \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) se usan para sincronizar el reenvío entre IGMP y los protocolos de enrutamiento.

 

 




