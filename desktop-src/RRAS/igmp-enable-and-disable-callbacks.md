---
title: Habilitar y deshabilitar devoluciones de llamada de IGMP
description: El administrador de grupos de multidifusión usa dos devoluciones de llamada a IGMP para coordinar los cambios en la propiedad de la interfaz de IGMP a un protocolo de enrutamiento, y de un protocolo de enrutamiento a IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103a0f9abb4d2a78b2b87fde3cb5832b4e88eb2677851d9fe703e5162263642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791148"
---
# <a name="igmp-enable-and-disable-callbacks"></a>Habilitar y deshabilitar devoluciones de llamada de IGMP

El administrador de grupos de multidifusión usa dos devoluciones de llamada a IGMP para coordinar los cambios en la propiedad de la interfaz de IGMP a un protocolo de enrutamiento, y de un protocolo de enrutamiento a IGMP. Las devoluciones de llamada permiten a IGMP coexistir en una interfaz con otro protocolo de enrutamiento, como DVMRP.

Una vez que cambia la propiedad de una interfaz, el administrador de grupos de multidifusión invoca primero la devolución de llamada [**PMGM \_ DISABLE \_ IGMP \_ CALLBACK.**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) IGMP debe detener la adición y eliminación de pertenencias a grupos en la interfaz especificada hasta que el administrador de grupos de multidifusión invoque la devolución de llamada DE DEvolución de llamada [**\_ DE PMGM ENABLE \_ IGMP. \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

El administrador de grupos de multidifusión invoca la devolución de llamada [**PMGM \_ ENABLE \_ IGMP \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) una vez completado el cambio de propiedad de la interfaz.

 

 