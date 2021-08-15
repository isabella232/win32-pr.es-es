---
title: Devoluciones de llamada de permiso locales
description: Después de que IGMP notifique al administrador de grupos de multidifusión que no hay más receptores presentes para un grupo en una interfaz, el administrador de grupos de multidifusión invoca la devolución de llamada PMGM LOCAL LEAVE CALLBACK al protocolo de enrutamiento en esa interfaz si existe \_ \_ \_ alguna. Esta devolución de llamada notifica el cambio al protocolo de enrutamiento.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4cd346ac3d84a5c763c7f8f866e21a1bffa2af533e5710c86ec8826ad7db45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790645"
---
# <a name="local-leave-callbacks"></a>Devoluciones de llamada de permiso locales

Después de que IGMP notifique al administrador de grupos de multidifusión que no hay más receptores presentes para un grupo en una interfaz, el administrador de grupos de multidifusión invoca la devolución de llamada [**PMGM \_ LOCAL LEAVE \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) al protocolo de enrutamiento en esa interfaz si existe alguna. Esta devolución de llamada notifica el cambio al protocolo de enrutamiento.

Esta devolución de llamada y la devolución de llamada [**PMGM \_ LOCAL JOIN \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) se usan para sincronizar el reenvío entre IGMP y los protocolos de enrutamiento.

 

 




