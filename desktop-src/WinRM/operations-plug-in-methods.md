---
title: Métodos del complemento de operaciones
description: Métodos del complemento de operaciones
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993804"
---
# <a name="operations-plug-in-methods"></a>Métodos del complemento de operaciones

Todos los puntos de entrada del complemento de operaciones tienen un mecanismo de devolución de llamada para notificar si la llamada se ha realizado correctamente o no. Algunos mecanismos de devolución de llamada se llaman varias veces, hasta que se notifiquen todos los resultados.

En la tabla siguiente se proporciona información general sobre los métodos de devolución de llamada de operaciones.



| Método                                                                         | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Libera la memoria asignada para la estructura de [**\_ \_ solicitud del complemento WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Obtiene información operativa, como tiempos de espera y restricciones de datos asociados a una operación.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Registra la finalización de una operación.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Informa de los resultados a Administración remota de Windows (WinRM) complementos.                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Devuelve el Shell y el contexto del comando a la infraestructura de WinRM para que se puedan realizar más operaciones con el shell o el comando. |



 

 

 




