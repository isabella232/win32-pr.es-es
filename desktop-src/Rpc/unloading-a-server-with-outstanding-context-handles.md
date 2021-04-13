---
title: Descargar un servidor con identificadores de contexto pendientes
description: Tradicionalmente, la descarga de un archivo DLL que atiende llamadas RPC con identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemática.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269296"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Descargar un servidor con identificadores de contexto pendientes

Tradicionalmente, la descarga de un archivo DLL que atiende llamadas RPC con identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemática. Esto se debe a que la rutina de ejecución ya no es válida cuando se descarga el archivo DLL. Cuando se produce un error en un cliente con un identificador de contexto abierto previamente, y el tiempo de ejecución de RPC intenta cerrar el identificador de contexto, su intento de llamar al acceso a la rutina de ejecución infringe y el servidor se bloquea.

A partir de Windows XP, se ha agregado una nueva API denominada [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) . **RpcServerUnregisterIfEx** cierra los identificadores de contexto abiertos por la interfaz que se va a eliminar del registro. la función [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) no lo hace. El uso de **RpcServerUnregisterIfEx** no es necesario cuando se cierra todo el proceso, pero es necesario si se descargan uno o varios archivos DLL que hospedan las rutinas de ejecución mientras existan identificadores de contexto pendientes.

 

 




