---
title: Devoluciones de llamada del administrador de grupo de multidifusión
description: El administrador del grupo de multidifusión usa las siguientes devoluciones de llamada para notificar a los clientes (normalmente, los protocolos de enrutamiento) de eventos y cambios de estado.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904713"
---
# <a name="multicast-group-manager-callbacks"></a>Devoluciones de llamada del administrador de grupo de multidifusión

El administrador del grupo de multidifusión usa las siguientes devoluciones de llamada para notificar a los clientes (normalmente, los protocolos de enrutamiento) de eventos y cambios de estado:

[**\_devolución de \_ llamada de alerta de creación de PMGM \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**\_devolución de \_ llamada de alerta de combinación de PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**\_devolución de \_ llamada de alerta de eliminación de PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**\_devolución de \_ llamada de combinación local de PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**\_devolución de \_ llamada de Leave local de PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**devolución de llamada de \_ RPF PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ incorrecto \_ si la \_ devolución de llamada**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

El administrador del grupo de multidifusión usa las siguientes devoluciones de llamada para notificar a IGMP de eventos y cambios de estado:

[**PMGM \_ deshabilitar \_ \_ devolución de llamada IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ habilitar \_ \_ devolución de llamada IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 