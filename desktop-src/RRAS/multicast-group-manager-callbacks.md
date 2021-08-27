---
title: Devoluciones de llamada del Administrador de grupos de multidifusión
description: El administrador de grupos de multidifusión usa las siguientes devoluciones de llamada para notificar a los clientes (normalmente, protocolos de enrutamiento) de eventos y cambios de estado.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037281a2cb636b337c5133c2c3a261e2c435a136a30d0ccfdcf0407a9b62509b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036655"
---
# <a name="multicast-group-manager-callbacks"></a>Devoluciones de llamada del Administrador de grupos de multidifusión

El administrador de grupos de multidifusión usa las siguientes devoluciones de llamada para notificar a los clientes (normalmente, protocolos de enrutamiento) de eventos y cambios de estado:

[**DEVOLUCIÓN DE LLAMADA \_ DE ALERTA DE CREACIÓN \_ \_ DE PMGM**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**DEVOLUCIÓN DE LLAMADA \_ DE ALERTA DE COMBINACIÓN \_ DE PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**DEVOLUCIÓN DE LLAMADA DE ALERTA DE PMGM \_ PRUNE \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**DEVOLUCIÓN DE \_ LLAMADA DE COMBINACIÓN LOCAL \_ PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**DEVOLUCIÓN DE \_ LLAMADA DE LA LICENCIA LOCAL \_ \_ DE PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**DEVOLUCIÓN DE \_ LLAMADA DE RPF DE PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ INCORRECTO SI \_ DEVOLUCIÓN DE \_ LLAMADA**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

El administrador de grupos de multidifusión usa las devoluciones de llamada siguientes para notificar a IGMP los eventos y los cambios de estado:

[**DEVOLUCIÓN DE LLAMADA \_ DE \_ IGMP \_ DESHABILITADA POR PMGM**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**DEVOLUCIÓN DE LLAMADA \_ DE PMGM ENABLE \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 