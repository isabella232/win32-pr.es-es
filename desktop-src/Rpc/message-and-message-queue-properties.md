---
title: Propiedades de cola de mensajes y mensajes
description: Un mensaje tiene propiedades, que especifican una etiqueta, un cuerpo del mensaje y una serie de opciones.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244443"
---
# <a name="message-and-message-queue-properties"></a>Propiedades de cola de mensajes y mensajes

Un mensaje tiene propiedades, que especifican una etiqueta, un cuerpo del mensaje y una serie de opciones. Las opciones de propiedad del mensaje pueden incluir calidad de servicio, prioridad, diario, niveles de privacidad y autenticación, y la duración del mensaje. En las aplicaciones de mensajes convencionales (que no son RPC), puede especificar estas propiedades mediante una llamada a las funciones de la API de MSMQ o a los métodos de objetos COM, que se describen en la documentación del SDK de MSMQ. Las aplicaciones cliente RPC pueden establecer determinadas propiedades para las llamadas a procedimientos remotos llamando a [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) y [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Una vez establecidas, las propiedades permanecen en vigor para cada mensaje hasta que la aplicación cliente las restablezca.

Una cola de mensajes tiene su propio conjunto de propiedades, aparte de las de los mensajes. Estas propiedades identifican de forma única una cola y definen la clase de servicio que proporciona la cola, los niveles de privacidad y autenticación necesarios para los mensajes de esta cola y si los mensajes van a formar parte de una transacción distribuida. Al igual que con las propiedades del mensaje, las propiedades de una cola de mensajes se especifican mediante una llamada a las funciones de la API de MSMQ o a los métodos de objeto COM, que se describen en la documentación de MSMQ. Sin embargo, una aplicación de servidor RPC puede especificar propiedades de su propia cola de recepción cuando llama a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) para establecer el enlace.

 

 




