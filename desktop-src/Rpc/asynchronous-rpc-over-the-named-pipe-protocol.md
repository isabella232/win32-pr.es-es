---
title: RPC asincrónica a través del Named-Pipe protocolo
description: Si usa canalizaciones con nombre (ncacn np) como protocolo de transporte, debe evitar permitir un gran número de llamadas inactivas \_ pendientes en el servidor.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1dade78846bc978abeb8bbbe5c324144db2645177722ca5afd1a62f99a3ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023675"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>RPC asincrónica a través del Named-Pipe protocolo

Si usa canalizaciones con nombre [**(ncacn \_ np**](/windows/desktop/Midl/ncacn-np)) como protocolo de transporte, debe evitar permitir un gran número de llamadas inactivas pendientes en el servidor. Con las canalizaciones con nombre, cada cliente que espera una respuesta tendrá una canalización con nombre pendiente leída en el servidor, cada una de las cuales requiere una cierta cantidad de memoria del kernel.

Por ejemplo, no le gustaría usar una llamada de notificación para el nuevo correo electrónico con el transporte de canalización con nombre, ya que dicha llamada permanecería pendiente incluso cuando los clientes están inactivos y la memoria del kernel podría agotarse. Tenga en cuenta que esto no es un problema con los demás protocolos orientados a la conexión, como [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp).

Puesto que las canalizaciones con nombre son un protocolo de transporte, la aplicación puede usarlas [**especificando ncacn \_ np**](/windows/desktop/Midl/ncacn-np) como protocolo en un enlace de cadena. Para obtener más información sobre las canalizaciones con nombre, vea [Canalizaciones con nombre.](/windows/desktop/ipc/named-pipes) Para obtener más información sobre cómo crear enlaces de cadena, vea [Usar enlaces de cadena.](finding-server-host-systems.md)

 

 