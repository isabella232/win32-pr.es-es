---
title: Limpieza del lado servidor
description: Limpieza del lado servidor y llamada a procedimiento remoto (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473524"
---
# <a name="server-side-cleanup"></a>Limpieza del lado servidor

Imagine el siguiente escenario:

Un cliente abre un identificador de contexto y, a continuación, detiene o pierde la conectividad con el servidor. ¿Cómo detecta el servidor que el cliente ha dado error y se debe ejecutar el identificador de contexto? Hay dos subscenarios: uno es que el cliente se apaga de forma ordenada. En tal caso, notifica al servidor que se está cerrando y el servidor puede limpiarlo, incluida la realización de las operaciones de ejecución de contexto. Si el cliente no se cierra de forma ordenada o no puede notificar al servidor, el servidor usa keep alives para determinar si el cliente sigue estando disponible. En el lado servidor, la [**función RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) no tiene ningún efecto. En su lugar, el servidor usa la configuración global por equipo y mantener activo, que tiene como valor predeterminado aproximadamente dos horas. Si el cliente no responde a los mensajes keep alive del servidor, la conexión se cierra. Cuando se cierran todas las conexiones a un proceso de cliente determinado, el servidor limpia y ejecuta los identificadores de contexto pendientes.

 

 




