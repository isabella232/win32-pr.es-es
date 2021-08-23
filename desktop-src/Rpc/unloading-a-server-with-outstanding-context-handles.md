---
title: Descargar un servidor con identificadores de contexto pendientes
description: Tradicionalmente, descargar un archivo DLL que atiende llamadas RPC mediante identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemático.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e581ff142c7453f4a9e9f1e40a5ab9991257a350a84b2fcb2ea08a0e157288cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010953"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Descargar un servidor con identificadores de contexto pendientes

Tradicionalmente, descargar un archivo DLL que atiende llamadas RPC mediante identificadores de contexto, sin detener primero el proceso de hospedaje, ha sido problemático. Esto se debe a que la rutina de ejecución ya no es válida cuando se descarga el archivo DLL. Cuando se produce un error en un cliente con un identificador de contexto abierto previamente y el tiempo de ejecución de RPC intenta cerrar el identificador de contexto, se infringe su intento de llamar al acceso rutinario de ejecución y el servidor se bloquea.

A partir Windows XP, se ha agregado una nueva API denominada [**RpcServerUnregisterIfEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) **RpcServerUnregisterIfEx** cierra los identificadores de contexto abiertos por la interfaz que se está anulando el registro; La [**función RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) no lo hace. No es necesario usar **RpcServerUnregisterIfEx** cuando se cierra todo el proceso, pero es necesario si uno o varios archivos DLL que hospedan las rutinas de ejecución se descargan mientras existen identificadores de contexto pendientes.

 

 




