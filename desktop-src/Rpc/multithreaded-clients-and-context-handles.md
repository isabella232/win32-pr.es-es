---
title: Clientes multiproceso y controladores de contexto
description: Cuando hay un cliente multiproceso en el que varios subprocesos usan la misma instancia de identificador de contexto, el acceso a la instancia de identificador de contexto se serializa en el servidor de forma predeterminada.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078065"
---
# <a name="multithreaded-clients-and-context-handles"></a>Clientes multiproceso y controladores de contexto

Cuando hay un cliente multiproceso en el que varios subprocesos usan la misma instancia de identificador de contexto, el acceso a la instancia de identificador de contexto se serializa en el servidor de forma predeterminada. Esto evita que el administrador del servidor tenga que protegerse frente a otro subproceso del mismo cliente que cambia el contexto o el contexto que se está ejecutando mientras se envía una llamada. Sin embargo, en ciertos casos, la serialización puede afectar al rendimiento.

Tenga en cuenta lo siguiente: dos subprocesos de cliente invocan una llamada a procedimiento remoto que no cambia el estado del contexto (por ejemplo, la llamada simplemente obtiene algunos valores de la misma). No es necesario serializar dichas llamadas.

En estos casos, Windows XP ofrece un modelo de serialización en modo mixto, donde cada método se puede declarar para que tenga acceso exclusivo o compartido a un identificador de contexto. Para obtener más información, vea [control de contexto \_ \_ serialización](/windows/desktop/Midl/context-handle-serialize) y [ \_ identificador \_ de contexto](/windows/desktop/Midl/context-handle-noserialize) .

En las versiones de Windows anteriores a Windows XP, el único medio para permitir el acceso simultáneo a un identificador de contexto es llamar a la función [**RpcSsDontSerializeContext**](/previous-versions/aa378473(v=vs.80)) para permitir que se envíen varias llamadas en un único identificador de contexto. La llamada a la función **RpcSsDontSerializeContext** no deshabilita completamente la serialización; Cuando se produce un error de ejecución de contexto, la rutina de ejecución del contexto se ejecuta solo cuando se han completado todas las solicitudes de cliente pendientes. Una llamada a **RpcScDontSerializeContext** afecta a todo el proceso y no se revierte. No se recomienda usar **RpcScDontSerializeContext** en Windows XP y versiones posteriores; hace que el código de servidor sea muy complicado cuando se trabaja de forma confiable con condiciones de carrera inherentes en entornos completamente no serializados.

 

 