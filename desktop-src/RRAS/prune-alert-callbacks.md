---
title: Eliminar devoluciones de llamada de alerta
description: Cuando se notifica al administrador del grupo de multidifusión que los receptores están abandonando un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la alerta de eliminación de PMGM \_ \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076256"
---
# <a name="prune-alert-callbacks"></a>Eliminar devoluciones de llamada de alerta

Cuando se notifica al administrador del grupo de multidifusión que los receptores están abandonando un grupo en una interfaz, el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la [**\_ alerta de eliminación de \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) . Esta devolución de llamada notifica a los protocolos de enrutamiento que los clientes ya no pertenecen al grupo especificado. Por lo tanto, los protocolos de enrutamiento deben dejar de solicitar datos de multidifusión para los grupos especificados.

El administrador del grupo de multidifusión tiene un conjunto predefinido de reglas que se utilizan para determinar cuándo se invoca esta devolución de llamada. Estas reglas se basan en el tipo de solicitud de eliminación enviada por el cliente y en el orden en que se recibieron las solicitudes de eliminación.

## <a name="wildcard-prune-requests"></a>Solicitudes de eliminación de caracteres comodín

Cuando se recibe una eliminación de caracteres comodín para un grupo ( \* , g) y se quita la interfaz final del segundo al último cliente (es decir, cuando se conservan interfaces para un solo cliente), el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la alerta de eliminación de PMGM al cliente [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) restante. Después de quitar la interfaz final del último cliente (es decir, cuando no quedan otras interfaces), se invoca esta devolución de llamada para todos los demás clientes registrados con el administrador del grupo de multidifusión.

## <a name="source-specific-prune-requests"></a>Solicitudes de eliminación de Source-Specific

Cuando se recibe una eliminación específica del origen de un grupo (s, g), el administrador del grupo de multidifusión invoca la devolución de llamada de devolución de llamada de la alerta de eliminación de PMGM solo para el cliente que posee la interfaz de entrada hacia los orígenes. [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

 

 




