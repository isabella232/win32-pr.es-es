---
title: Descargar un servidor con identificadores de contexto pendientes
description: Tradicionalmente, descargar un archivo DLL que atiende llamadas RPC mediante identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemático.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071379"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Descargar un servidor con identificadores de contexto pendientes

Tradicionalmente, descargar un archivo DLL que atiende llamadas RPC mediante identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemático. Esto se debe a que la rutina de ejecución ya no es válida cuando se descarga el archivo DLL. Cuando se produce un error en un cliente con un identificador de contexto abierto previamente y el tiempo de ejecución rpc intenta cerrar el identificador de contexto, su intento de llamar al acceso rutinario de ejecución infringe y el servidor se bloquea.

A partir Windows XP, se ha agregado una nueva API denominada [**RpcServerUnregisterIfEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) **RpcServerUnregisterIfEx** cierra los identificadores de contexto abiertos por la interfaz que se está anulando el registro; La [**función RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) no lo hace. No es necesario usar **RpcServerUnregisterIfEx** cuando se cierra todo el proceso, pero es necesario si uno o varios archivos DLL que hospedan las rutinas de ejecución se descargan mientras existen identificadores de contexto pendientes.

 

 




