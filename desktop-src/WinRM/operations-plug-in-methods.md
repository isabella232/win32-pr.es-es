---
title: Métodos de complemento de operaciones
description: Métodos de complemento de operaciones
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bcfc2263a9ecd35c050499f0547b5bc5190e5896b430edabe6be8490239b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323897"
---
# <a name="operations-plug-in-methods"></a>Métodos de complemento de operaciones

Todos los puntos de entrada del complemento de operaciones tienen un mecanismo de devolución de llamada para notificar el éxito o el error de la llamada. Algunos mecanismos de devolución de llamada se llaman varias veces, hasta que se notifican todos los resultados.

En la tabla siguiente se proporciona información general sobre los métodos de devolución de llamada de operaciones.



| Método                                                                         | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Libera la memoria que se asigna para la estructura [**DE SOLICITUD DEL \_ COMPLEMENTO \_ WSMAN.**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Obtiene información operativa, como tiempos de espera y restricciones de datos asociadas a una operación.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Registra la finalización de una operación.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Notifica los resultados Windows complementos de administración remota (WinRM).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Notifica el shell y el contexto de comando a la infraestructura de WinRM para que se puedan realizar más operaciones en el shell o comando. |



 

 

 




