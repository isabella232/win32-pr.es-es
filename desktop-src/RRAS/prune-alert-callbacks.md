---
title: Devoluciones de llamada de alertas de prune
description: Cuando se notifica al administrador de grupos de multidifusión que los receptores abandonan un grupo en una interfaz, el administrador de grupos de multidifusión invoca la devolución de llamada PMGM \_ PRUNE \_ ALERT \_ CALLBACK.
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5aa4d95742a2976ea46367b0f1af9442528c2821dc9d27b09b9e1c29eee6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036405"
---
# <a name="prune-alert-callbacks"></a>Devoluciones de llamada de alertas de prune

Cuando se notifica al administrador de grupos de multidifusión que los receptores abandonan un grupo en una interfaz, el administrador de grupos de multidifusión invoca la devolución de llamada [**PMGM \_ PRUNE \_ ALERT \_ CALLBACK.**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Esta devolución de llamada notifica a los protocolos de enrutamiento que los clientes ya no pertenecen al grupo especificado. Por lo tanto, los protocolos de enrutamiento deben dejar de solicitar datos de multidifusión para los grupos especificados.

El administrador de grupos de multidifusión tiene un conjunto predefinido de reglas que se usan para determinar cuándo se invoca esta devolución de llamada. Estas reglas se basan en el tipo de solicitud de prune enviada por el cliente y en el orden en que se recibieron las solicitudes de prune.

## <a name="wildcard-prune-requests"></a>Solicitudes de prune con caracteres comodín

Cuando se recibe una eliminación de caracteres comodín para un grupo ( , g) y se quita la interfaz final para el segundo y último cliente (es decir, cuando solo permanecen las interfaces para un solo cliente), el administrador de grupos de multidifusión invoca la devolución de llamada DE DEvolución de llamada de ALERTA DE \* [**\_ PRUNE \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) a ese cliente restante. Después de quitar la interfaz final para el último cliente (es decir, cuando no quedan otras interfaces), se invoca esta devolución de llamada para todos los demás clientes registrados con el administrador de grupos de multidifusión.

## <a name="source-specific-prune-requests"></a>Source-Specific solicitudes de prune

Cuando se recibe una poda específica de origen para un grupo (s, g), el administrador de grupos de multidifusión invoca la devolución de llamada DE DEvolución de llamada [**PMGM \_ PRUNE \_ ALERT \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) solo para el cliente que posee la interfaz entrante hacia los de origen.

 

 




