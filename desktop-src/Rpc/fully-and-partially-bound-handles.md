---
title: Identificadores de enlace completo y parcialmente
description: Cuando se usan puntos de conexión dinámicos, las bibliotecas en tiempo de ejecución obtienen información del punto de conexión según lo necesiten.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486823"
---
# <a name="fully-and-partially-bound-handles"></a>Identificadores de enlace completo y parcialmente

Cuando se usan puntos de conexión dinámicos, las bibliotecas en tiempo de ejecución obtienen información del punto de conexión según lo necesiten. Las bibliotecas en tiempo de ejecución realizan la distinción entre un *identificador de enlace completo* (uno que incluye la información de extremo) y un *identificador de enlace parcial* (uno que no incluye información de extremo).

La biblioteca en tiempo de ejecución del cliente debe convertir el identificador de enlace parcial en un identificador de enlace completo antes de que el cliente pueda enlazar con el servidor. La biblioteca en tiempo de ejecución de cliente intenta convertir el identificador de enlace parcial para la aplicación cliente obteniendo la información del punto de conexión como se muestra:

-   Desde la especificación de interfaz del cliente
-   Desde un servicio de asignación de puntos de conexión que se ejecuta en el servidor

Si el cliente intenta utilizar un identificador de enlace parcial cuando la información del punto de conexión no está disponible en la especificación de interfaz y el asignador de extremos del servidor no tiene información sobre el punto de conexión del servidor, el cliente no tendrá suficiente información para realizar su llamada a procedimiento remoto y se producirá un error en la llamada. Para evitarlo, debe registrar el extremo en el asignador de extremos cuando la aplicación distribuida utiliza identificadores de enlace parcial. Para obtener más información acerca del asignador de extremos, consulte [especificar puntos de conexión dinámicos](specifying-endpoints.md).

Cuando se produce un error en una llamada a procedimiento remoto, la aplicación cliente puede llamar a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) para quitar la información de punto de conexión desactualizada. Cuando el cliente intenta llamar al procedimiento remoto, la biblioteca en tiempo de ejecución de cliente intenta convertir el identificador completamente enlazado en un identificador de enlace parcial. Esto resulta útil cuando el servidor se ha detenido y reiniciado con un punto de conexión dinámico diferente.

 

 




