---
title: RPC asincrónico a través del protocolo Named-Pipe
description: Si usa canalizaciones con nombre (ncacn \_ NP) como protocolo de transporte, debe evitar permitir un gran número de llamadas pendientes de inactividad en el servidor.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995553"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>RPC asincrónico a través del protocolo Named-Pipe

Si usa canalizaciones con nombre ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) como protocolo de transporte, debe evitar permitir un gran número de llamadas pendientes de inactividad en el servidor. Con las canalizaciones con nombre, cada cliente que espera una respuesta tendrá una canalización con nombre pendiente leída en el servidor, cada una de las cuales requiere una determinada cantidad de memoria del kernel.

Por ejemplo, no querrá usar una llamada de notificación para nuevos mensajes de correo electrónico con el transporte de canalización con nombre, ya que dicha llamada permanecerá pendiente incluso cuando los clientes estén inactivos y se podría agotar la memoria del kernel. Tenga en cuenta que esto no es un problema con los demás protocolos orientados a la conexión, como [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).

Dado que las canalizaciones con nombre son un protocolo de transporte, la aplicación puede usarlas especificando [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) como protocolo en un enlace de cadenas. Para obtener más información sobre las canalizaciones con nombre, vea [canalizaciones con nombre](/windows/desktop/ipc/named-pipes). Para obtener más información sobre cómo crear enlaces de cadena, vea [usar enlaces de cadena](finding-server-host-systems.md).

 

 