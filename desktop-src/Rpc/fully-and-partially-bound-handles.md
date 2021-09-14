---
title: Identificadores totalmente y parcialmente enlazados
description: Cuando se usan puntos de conexión dinámicos, las bibliotecas en tiempo de ejecución obtienen información de punto de conexión cuando la necesitan.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361935"
---
# <a name="fully-and-partially-bound-handles"></a>Identificadores totalmente y parcialmente enlazados

Cuando se usan puntos de conexión dinámicos, las bibliotecas en tiempo de ejecución obtienen información de punto de conexión cuando la necesitan. Las bibliotecas en tiempo de ejecución hacen la distinción entre un identificador totalmente enlazado *(uno* que incluye información de punto de conexión) y un identificador enlazado *parcialmente* (uno que no incluye información de punto de conexión).

La biblioteca en tiempo de ejecución del cliente debe convertir el identificador enlazado parcialmente en un identificador totalmente enlazado antes de que el cliente pueda enlazarse al servidor. La biblioteca en tiempo de ejecución del cliente intenta convertir el identificador enlazado parcialmente para la aplicación cliente obteniendo la información del punto de conexión como se muestra:

-   A partir de la especificación de la interfaz del cliente
-   Desde un servicio de asignación de puntos de conexión que se ejecuta en el servidor

Si el cliente intenta usar un identificador enlazado parcialmente cuando la información del punto de conexión no está disponible en la especificación de interfaz y el asignador de puntos de conexión del servidor no tiene información sobre el punto de conexión del servidor, el cliente no tendrá suficiente información para realizar su llamada a procedimiento remoto y se producirá un error en esa llamada. Para evitarlo, debe registrar el punto de conexión en el asignador de puntos de conexión cuando la aplicación distribuida usa identificadores enlazados parcialmente. Para obtener más información sobre el asignador de puntos de conexión, vea [Especificar puntos de conexión dinámicos.](specifying-endpoints.md)

Cuando se produce un error en una llamada a procedimiento remoto, la aplicación cliente puede llamar a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) para quitar la información de punto de conexión no actualizada. Cuando el cliente intenta llamar al procedimiento remoto, la biblioteca en tiempo de ejecución del cliente vuelve a intentar convertir el identificador totalmente enlazado en un identificador enlazado parcialmente. Esto resulta útil cuando el servidor se ha detenido y reiniciado mediante un punto de conexión dinámico diferente.

 

 




