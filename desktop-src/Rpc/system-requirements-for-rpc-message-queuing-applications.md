---
title: Requisitos del sistema para RPC-Message queuing Applications
description: Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalada la plataforma de sistema operativo adecuada y el software de Message Queuing.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476597"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisitos del sistema para RPC-Message queuing Applications

Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalada la plataforma de sistema operativo adecuada y el software de Message Queuing.

Los requisitos de los equipos servidor son:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.
-   SQL Server versión 6.5 o posterior.
-   Controlador principal Enterprise Message Queuing o controlador de sitio primario.
-   DLL de transporte del lado servidor RPC (RpcMqSvr.dll).

Los requisitos de los equipos cliente son:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.
-   Microsoft Message Queuing cliente.
-   DLL de transporte del lado cliente RPC (RpcMqCl.dll).

Cuando los componentes de MSMQ están instalados en los equipos cliente y servidor, los registros del sistema se configuran automáticamente para incluir el protocolo de transporte [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) message-queuing para las llamadas a procedimiento remoto.

Para compilar la aplicación RPC-MSMQ, necesita lo siguiente:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior
-   MIDL versión 3.1.76 o posterior.

 

 