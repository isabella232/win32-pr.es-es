---
title: Combinaciones de devoluciones de llamada de alerta
description: Cuando se notifica al administrador de grupos de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador de grupos de multidifusión invoca la devolución de llamada DE DEvolución de llamada DE ALERTA DE COMBINACIÓN DE \_ \_ \_ PMGM.
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0da66e405441804cbca4452cedd7a6599067138bee95a33eaee7a2f10c34c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074125"
---
# <a name="join-alert-callbacks"></a>Combinaciones de devoluciones de llamada de alerta

Cuando se notifica al administrador de grupos de multidifusión que hay nuevos receptores para un grupo en una interfaz, el administrador de grupos de multidifusión invoca la devolución de llamada DE DEvolución de llamada DE ALERTA DE COMBINACIÓN DE [**PMGM. \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) Esta devolución de llamada notifica a los protocolos de enrutamiento que los nuevos hosts se han unido a los grupos especificados. Por lo tanto, los protocolos de enrutamiento deben solicitar datos de multidifusión para los grupos especificados por la devolución de llamada.

El administrador de grupos de multidifusión usa un conjunto predefinido de reglas que se usan para determinar cuándo se invoca esta devolución de llamada. Este conjunto de reglas se basa en el tipo de solicitud de combinación enviada por el cliente y en el orden en que se recibieron las solicitudes de combinación.

## <a name="wildcard-join-requests"></a>Solicitudes de combinación de caracteres comodín

Cuando se recibe una combinación con caracteres comodín para un grupo ( , g) del primer cliente, el administrador de grupos de multidifusión invoca la devolución de llamada \* [**PMGM \_ JOIN ALERT \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) a todos los demás clientes registrados. Cuando se recibe una combinación de caracteres comodín para un grupo desde el segundo cliente, el administrador de grupos de multidifusión invoca esta devolución de llamada al primer cliente que se une al grupo.

## <a name="source-specific-join-requests"></a>Source-Specific solicitudes de unión

El administrador de grupos de multidifusión no invoca esta devolución de llamada para las combinaciones posteriores al grupo.

Cuando se recibe una combinación específica de origen para un grupo (s, g), el administrador de grupos de multidifusión invoca la devolución de llamada [**PMGM \_ JOIN ALERT \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) solo para el cliente que posee la interfaz entrante hacia los de origen.

 

 




