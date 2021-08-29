---
title: Métodos de complemento de autorización
description: Todos los puntos de entrada del complemento de autorización tienen un mecanismo de devolución de llamada para notificar el éxito o el error de la llamada. Algunos mecanismos de devolución de llamada se llaman varias veces hasta que se notifican todos los resultados.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db09430d83e91a8df25dbbc09607c3a9ac3cad266f3a15c1738565c651271b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955335"
---
# <a name="authorization-plug-in-methods"></a>Métodos de complemento de autorización

Todos los puntos de entrada del complemento de autorización tienen un mecanismo de devolución de llamada para notificar el éxito o el error de la llamada. Algunos mecanismos de devolución de llamada se llaman varias veces hasta que se notifican todos los resultados.

En la tabla siguiente se proporciona información general sobre los métodos de devolución de llamada de autorización.



| Método                                                                           | Descripción                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Informa de una operación de usuario correcta o con errores.                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Notifica los detalles de cuota que son pertinentes para el usuario especificado.      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Notifica una autorización de conexión de usuario correcta o con errores. |



 

 

 




