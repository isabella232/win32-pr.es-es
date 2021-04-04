---
title: Usar MSMQ como transporte RPC
description: El subsistema RPC admite el uso de MSMQ como transporte en modos sincrónicos y asincrónicos.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a647fe4111e3ba4fc2ad0fe05fb7bcb48729a4c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793125"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Usar MSMQ como transporte RPC

El subsistema RPC admite el uso de MSMQ como transporte en modos sincrónicos y asincrónicos.

El modo sincrónico utiliza las llamadas a procedimiento remoto convencionales. Estas llamadas usan puntos de conexión conocidos y el transporte de cola de mensajes, [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq), como protocolo de transporte. En el modo sincrónico, los procedimientos remotos pueden tener \[ parámetros [in](/windows/desktop/Midl/in) \] y \[ [out](/windows/desktop/Midl/out-idl) \] y pueden usar los servicios de seguridad RPC estándar. El subsistema RPC crea una cola de respuestas para llamadas remotas que contienen parámetros **\[ out \]** . El modo sincrónico es útil para las aplicaciones en las que el cliente necesita recibir datos del servidor. La principal limitación de este modo es que, al igual que con las llamadas a procedimientos remotos convencionales, el cliente y el servidor deben estar en ejecución y seguir ejecutándose mientras dure la llamada.

El modo asincrónico permite a las aplicaciones cliente realizar llamadas al servidor y volver inmediatamente, independientemente del estado de la aplicación de servidor o del equipo servidor. También hace que un subconjunto de características de MSMQ esté disponible para administrar las colas de mensajes y el flujo de información. La función [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) permite controlar la calidad de servicio, la prioridad de llamadas, el registro en diario, la seguridad y la duración de la cola de procesos del servidor. La función [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) permite especificar atributos de la cola de procesos de servidor, como la persistencia de colas, la autenticación y el cifrado.

Se implementa MSMQ asincrónico como lo haría con MSMQ sincrónico. Debe usar puntos de conexión conocidos y definir el protocolo de transporte para que sea [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq). En el archivo IDL, aplique el atributo [Message](/windows/desktop/Midl/message) a las funciones que utilizan Message Queue Server asincrónico. Tenga en cuenta que las funciones \[ de mensaje solo pueden tener \] parámetros in.

 

 