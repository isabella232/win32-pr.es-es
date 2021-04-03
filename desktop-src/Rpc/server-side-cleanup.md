---
title: Limpieza del lado servidor
description: Limpieza del lado servidor y llamada a procedimiento remoto (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075981"
---
# <a name="server-side-cleanup"></a>Limpieza del lado servidor

Imagínese el siguiente escenario:

Un cliente abre un identificador de contexto y, a continuación, se detiene o pierde la conectividad con el servidor. ¿Cómo detecta el servidor que se ha producido un error en el cliente y se debe ejecutar el identificador de contexto? Hay dos subescenarios: uno es que el cliente se cierra de forma ordenada. En tal caso, notifica al servidor que se está cerrando y el servidor puede realizar la limpieza, incluida la realización de las ejecuciones de contexto. Si el cliente no se cierra de forma ordenada o no puede notificar al servidor, el servidor usa Keep alives para determinar si el cliente sigue estando disponible. En el lado del servidor, la función [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) no tiene ningún efecto. En su lugar, el servidor usa la configuración global por máquina: Keep Alive, que tiene como valor predeterminado dos horas aproximadamente. Si el cliente no responde a las conexiones de mantenimiento del servidor, la conexión está cerrada. Cuando se cierran todas las conexiones a un proceso de cliente determinado, el servidor limpia y ejecuta los identificadores de contexto pendientes.

 

 




