---
title: Métodos de complemento de autorización
description: Todos los puntos de entrada del complemento de autorización tienen un mecanismo de devolución de llamada para notificar si la llamada se ha realizado correctamente o no. Se llama varias veces a algunos mecanismos de devolución de llamada hasta que se notifiquen todos los resultados.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704661"
---
# <a name="authorization-plug-in-methods"></a>Métodos de complemento de autorización

Todos los puntos de entrada del complemento de autorización tienen un mecanismo de devolución de llamada para notificar si la llamada se ha realizado correctamente o no. Se llama varias veces a algunos mecanismos de devolución de llamada hasta que se notifiquen todos los resultados.

En la tabla siguiente se proporciona información general sobre los métodos de devolución de llamada de autorización.



| Método                                                                           | Descripción                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Informa de una operación de usuario correcta o errónea.                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Informa de los detalles de la cuota relevantes para el usuario especificado.      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Informa de una autorización de conexión de usuario correcta o errónea. |



 

 

 




