---
title: Clientes multiproceso y identificadores de contexto
description: Cuando tiene un cliente multiproceso en el que varios subprocesos usan la misma instancia de identificador de contexto, el acceso a la instancia del identificador de contexto se serializa en el servidor de forma predeterminada.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7fed15deacca47754f51869fa0b18b37135586addb7f80b8aa75b9dde63082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928094"
---
# <a name="multithreaded-clients-and-context-handles"></a>Clientes multiproceso y identificadores de contexto

Cuando tiene un cliente multiproceso en el que varios subprocesos usan la misma instancia de identificador de contexto, el acceso a la instancia del identificador de contexto se serializa en el servidor de forma predeterminada. Esto hace que el administrador del servidor no tenga que protegerse contra otro subproceso desde el mismo cliente, cambiando el contexto o el contexto que se está ejecutando mientras se envía una llamada. Sin embargo, en algunos casos, la serialización puede afectar al rendimiento.

Tenga en cuenta lo siguiente: dos subprocesos de cliente invocan una llamada a procedimiento remoto que no cambia el estado del contexto (por ejemplo, la llamada simplemente obtiene algunos valores de él). No es necesario serializar estas llamadas.

En tales situaciones, Windows XP ofrece un modelo de serialización en modo mixto, donde cada método se puede declarar para tener acceso exclusivo o compartido a un identificador de contexto. Consulte [serialización \_ de identificador de \_ contexto](/windows/desktop/Midl/context-handle-serialize) y [ \_ \_ noserialize del identificador](/windows/desktop/Midl/context-handle-noserialize) de contexto para obtener más información.

En versiones de Windows anteriores a Windows XP, el único medio de permitir el acceso simultáneo a un identificador de contexto es llamar a la función [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) para permitir que varias llamadas se envíen en un único identificador de contexto. Llamar a **la función RpcSsDontSerializeContext** no deshabilita completamente la serialización; cuando se produce una ejecución de contexto, la rutina de ejecución de contexto se ejecuta solo cuando se han completado todas las solicitudes de cliente pendientes. Una llamada a **RpcScDontSerializeContext** afecta a todo el proceso y no se puede revertir. No **se recomienda usar RpcScDontSerializeContext** Windows XP y versiones posteriores; hace que el código del servidor sea muy complicado cuando se trabaja de forma confiable con condiciones de carrera inherentes a entornos completamente no serializados.

 

 