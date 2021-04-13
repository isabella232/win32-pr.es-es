---
title: Requisitos del sistema para aplicaciones de RPC-Message Queue Server
description: Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalado el software de plataforma de sistema operativo y de Message Queue Server adecuado.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421227"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Requisitos del sistema para aplicaciones de RPC-Message Queue Server

Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalado el software de plataforma de sistema operativo y de Message Queue Server adecuado.

Los requisitos de los equipos servidor son:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.
-   SQL Server versión 6,5 o posterior.
-   Controlador Enterprise principal de Message Queue Server o controlador de sitio primario.
-   DLL de transporte del lado servidor RPC (RpcMqSvr.dll).

Los requisitos de los equipos cliente son los siguientes:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.
-   Microsoft Message Queuing cliente.
-   DLL de transporte del lado cliente RPC (RpcMqCl.dll).

Cuando los componentes de MSMQ se instalan en los equipos cliente y servidor, los registros del sistema se configuran automáticamente para incluir el protocolo de transporte [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) Message-Queue Transport para llamadas a procedimientos remotos.

Para compilar la aplicación RPC-MSMQ necesita lo siguiente:

-   Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior
-   Versión de MIDL 3.1.76 o posterior.

 

 