---
title: Requisitos del sistema para RPC-Message queuing Applications
description: Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalada la plataforma de sistema operativo adecuada y el software de Message Queuing.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46d9775e720c725ad3b0d06a0be0cf67aa438f739c6a0d1162f4940ac59e561e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924652"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisitos del sistema para RPC-Message queuing Applications

Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalada la plataforma de sistema operativo adecuada y el software de Message Queuing.

Los requisitos de los equipos servidor son:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.
-   SQL Server versión 6.5 o posterior.
-   Controlador principal Enterprise Message Queuing o controlador de sitio principal.
-   DLL de transporte del lado servidor RPC (RpcMqSvr.dll).

Los requisitos de los equipos cliente son:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.
-   Microsoft Message Queuing cliente.
-   DLL de transporte del lado cliente RPC (RpcMqCl.dll).

Cuando los componentes de MSMQ están instalados en los equipos cliente y servidor, los registros del sistema se configuran automáticamente para incluir el protocolo de transporte [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) message-queuing para las llamadas a procedimiento remoto.

Para compilar la aplicación RPC-MSMQ, necesita lo siguiente:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior
-   MIDL versión 3.1.76 o posterior.

 

 