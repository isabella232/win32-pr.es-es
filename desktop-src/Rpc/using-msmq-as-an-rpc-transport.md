---
title: Uso de MSMQ como transporte RPC
description: El subsistema RPC admite el uso de MSMQ como transporte en modos sincrónicos y asincrónicos.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab18f4476815929e8a7e6fb4e4a1eef0a4e4e34754ac134f023c8551899e0138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010683"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Uso de MSMQ como transporte RPC

El subsistema RPC admite el uso de MSMQ como transporte en modos sincrónicos y asincrónicos.

El modo sincrónico usa llamadas a procedimientos remotos convencionales. Estas llamadas usan puntos de conexión conocidos y el transporte de la cola de mensajes, [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq), como protocolo de transporte. En modo sincrónico, los procedimientos remotos pueden tener parámetros de entrada y \[ [](/windows/desktop/Midl/in) \] salida y pueden usar \[ [](/windows/desktop/Midl/out-idl) \] los servicios de seguridad RPC estándar. El subsistema RPC crea una cola de respuesta para las llamadas remotas que contienen **\[ parámetros out. \]** El modo sincrónico es útil para las aplicaciones en las que el cliente necesita recibir datos del servidor. La limitación principal de este modo es que, al igual que con las llamadas a procedimientos remotos convencionales, tanto el cliente como el servidor deben estar en ejecución y permanecer en ejecución mientras dure la llamada.

El modo asincrónico permite a las aplicaciones cliente realizar llamadas al servidor y devolver inmediatamente, independientemente del estado de la aplicación de servidor o del equipo servidor. También hace que un subconjunto de características de MSMQ esté disponible para administrar las colas de mensajes y el flujo de información. La [**función RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) permite controlar la calidad del servicio, la prioridad de llamada, el registro en diario, la seguridad y la duración de la cola de procesos del servidor. La [**función RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) permite especificar atributos de la cola de procesos del servidor, como la persistencia de la cola, la autenticación y el cifrado.

Implemente MSMQ asincrónico como haría con MSMQ sincrónico. Debe usar puntos de conexión conocidos y definir el protocolo de transporte para que [sea ncadg \_ mq](/windows/desktop/Midl/ncadg-mq). En el archivo IDL, aplique el atributo [de mensaje](/windows/desktop/Midl/message) a las funciones que usan la cola de mensajes asincrónica. Tenga en cuenta que las funciones de mensaje solo \[ pueden tener \] en parámetros.

 

 