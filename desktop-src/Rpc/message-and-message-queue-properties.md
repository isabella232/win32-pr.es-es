---
title: Propiedades de Message y Message Queue
description: Un mensaje tiene propiedades, que especifican una etiqueta, un cuerpo de mensaje y varias opciones.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357341"
---
# <a name="message-and-message-queue-properties"></a>Propiedades de Message y Message Queue

Un mensaje tiene propiedades, que especifican una etiqueta, un cuerpo de mensaje y varias opciones. Las opciones de propiedad del mensaje pueden incluir la calidad de servicio, la prioridad, el registro en diario, los niveles de privacidad y autenticación, y la duración del mensaje. En las aplicaciones de Message Queue Server (no RPC) convencionales, estas propiedades se especifican mediante una llamada a las funciones de la API de MSMQ o a los métodos de objeto COM, que se describen en la documentación del SDK de MSMQ. Las aplicaciones cliente RPC pueden establecer determinadas propiedades para llamadas a procedimientos remotos llamando a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) y [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Una vez establecidas, las propiedades permanecen en vigor para cada mensaje hasta que la aplicación cliente las restablece.

Una cola de mensajes tiene su propio conjunto de propiedades, además de los de los mensajes. Estas propiedades identifican de forma única una cola y definen la clase de servicio que proporciona la cola, los niveles de privacidad y autenticación necesarios para los mensajes de esta cola, y si los mensajes van a formar parte de una transacción distribuida. Al igual que con las propiedades del mensaje, se especifican las propiedades de una cola de mensajes mediante una llamada a las funciones de la API de MSMQ o a los métodos de objeto COM, que se describen en la documentación de MSMQ. Sin embargo, una aplicación de servidor RPC puede especificar propiedades de su propia cola de recepción cuando llama a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) para establecer el enlace.

 

 




