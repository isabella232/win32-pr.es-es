---
title: Combinar devoluciones de llamada de alerta
description: Cuando se notifica al administrador del grupo de multidifusión que hay nuevos receptores presentes para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de alerta de combinación de PMGM \_ \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075938"
---
# <a name="join-alert-callbacks"></a>Combinar devoluciones de llamada de alerta

Cuando se notifica al administrador del grupo de multidifusión que hay nuevos receptores presentes para un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de [**devolución de llamada de alerta de combinación de PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) . Esta devolución de llamada notifica a los protocolos de enrutamiento que los nuevos hosts se han unido a los grupos especificados. Por lo tanto, los protocolos de enrutamiento deben solicitar datos de multidifusión para los grupos especificados por la devolución de llamada.

El administrador del grupo de multidifusión usa un conjunto predefinido de reglas que se utilizan para determinar cuándo se invoca esta devolución de llamada. Este conjunto de reglas se basa en el tipo de solicitud de combinación enviada por el cliente y en el orden en que se recibieron las solicitudes de Unión.

## <a name="wildcard-join-requests"></a>Solicitudes de combinación comodín

Cuando se recibe una combinación de caracteres comodín para un grupo ( \* , g) del primer cliente, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de alerta de combinación de PMGM a todos los demás clientes registrados. [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) Cuando se recibe una combinación de caracteres comodín para un grupo desde el segundo cliente, el administrador del grupo de multidifusión invoca esta devolución de llamada al primer cliente para unirse al grupo.

## <a name="source-specific-join-requests"></a>Solicitudes de Source-Specific join

El administrador del grupo de multidifusión no invoca esta devolución de llamada para las combinaciones posteriores al grupo.

Cuando se recibe una combinación específica del origen para un grupo (s, g), el administrador del grupo de multidifusión invoca la devolución de llamada de [**devolución de llamada de alerta de PMGM \_ join \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) solo para el cliente que posee la interfaz de entrada hacia los orígenes.

 

 




