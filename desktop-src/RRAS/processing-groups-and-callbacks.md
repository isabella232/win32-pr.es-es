---
title: Grupos de procesamiento y devoluciones de llamada
description: En la tabla siguiente se resume una serie de pasos en una interacción operativa entre un protocolo de enrutamiento y el administrador de grupos de multidifusión.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3315f0a5db0dbcef9ac13e07ff9b9a2bb0b476be
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479691"
---
# <a name="processing-groups-and-callbacks"></a>Grupos de procesamiento y devoluciones de llamada

En la tabla siguiente se resume una serie de pasos en una interacción operativa entre un protocolo de enrutamiento y el administrador de grupos de multidifusión. En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del protocolo de enrutamiento al administrador de grupos de multidifusión. En la segunda columna se describen las respuestas del administrador de grupos de multidifusión al protocolo de enrutamiento y las acciones que realiza el administrador de grupos de multidifusión, como las devoluciones de llamada. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.

Las tareas enumeradas en esta tabla no se producen en ningún orden específico; en su lugar, se producen en función del estado de las pertenencias a grupos de multidifusión. En la tabla siguiente se muestra un orden de ejemplo.




| Acción del protocolo de enrutamiento | Acción del administrador de grupos de multidifusión | Notas | 
|-------------------------|--------------------------------|-------|
| Administre las pertenencias a grupos en función de la información de protocolo recibida en esas interfaces que posee el protocolo. La administración se realiza mediante las siguientes funciones:<ul><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li></ul> | Agregue y elimine de la lista de interfaces de salida para las entradas especificadas (s, g), (*, g)* y ( , *) . Esta lista representa el conjunto de interfaces en las que se reenvía los datos de este grupo. Los datos de este grupo son del origen especificado. | 
| Envíe alertas a los protocolos de enrutamiento en forma de devoluciones de llamada. Los siguientes eventos desencadenan el administrador de grupos de multidifusión para invocar una devolución de llamada:<ul><li>Unirse o salir de grupos ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li><li>La pertenencia a grupos cambiada por IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li><li>Datos recibidos en una interfaz incorrecta ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li><li>Datos recibidos de nuevos orígenes o de un nuevo grupo <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>(PMGM_CREATION_ALERT_CALLBACK</strong></a> y <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li></ul> | Con estas devoluciones de llamada, el administrador de grupos de multidifusión puede coordinar el reenvío de paquetes cuando hay varios protocolos de enrutamiento de multidifusión en un enrutador. | 
| Enumerar las entradas de reenvío de multidifusión (MFE), mediante las funciones <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>y <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe.</strong></a> Tome decisiones sobre los datos de multidifusión en función de los resultados de la enumeración . | Devuelve las mfes solicitadas. Devuelve ERROR_NO_MORE elementos cuando no hay más MFE para devolver.<br /> | Use las <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>funciones MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> para enumerar las estadísticas de MFE. Consulte <a href="administrative-application-scenario.md">Escenario de aplicación administrativa</a> para obtener un ejemplo completo del uso de estas funciones.<br /> | 
| Modifique el vecino ascendente en un MFE mediante la <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>función MgmSetMfe.</strong></a> | Los clientes usan esta función para modificar la información relacionada con la interfaz entrante. | 




 

 

