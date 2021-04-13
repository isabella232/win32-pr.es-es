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
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="6a225-103">Requisitos del sistema para aplicaciones de RPC-Message Queue Server</span><span class="sxs-lookup"><span data-stu-id="6a225-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="6a225-104">Para usar el transporte de cola de mensajes en una aplicación cliente/servidor RPC, los equipos cliente y servidor deben tener instalado el software de plataforma de sistema operativo y de Message Queue Server adecuado.</span><span class="sxs-lookup"><span data-stu-id="6a225-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="6a225-105">Los requisitos de los equipos servidor son:</span><span class="sxs-lookup"><span data-stu-id="6a225-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="6a225-106">Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6a225-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="6a225-107">SQL Server versión 6,5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6a225-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="6a225-108">Controlador Enterprise principal de Message Queue Server o controlador de sitio primario.</span><span class="sxs-lookup"><span data-stu-id="6a225-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="6a225-109">DLL de transporte del lado servidor RPC (RpcMqSvr.dll).</span><span class="sxs-lookup"><span data-stu-id="6a225-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="6a225-110">Los requisitos de los equipos cliente son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6a225-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="6a225-111">Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6a225-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="6a225-112">Microsoft Message Queuing cliente.</span><span class="sxs-lookup"><span data-stu-id="6a225-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="6a225-113">DLL de transporte del lado cliente RPC (RpcMqCl.dll).</span><span class="sxs-lookup"><span data-stu-id="6a225-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="6a225-114">Cuando los componentes de MSMQ se instalan en los equipos cliente y servidor, los registros del sistema se configuran automáticamente para incluir el protocolo de transporte [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) Message-Queue Transport para llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="6a225-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="6a225-115">Para compilar la aplicación RPC-MSMQ necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a225-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="6a225-116">Microsoft Windows Server 2003, Windows XP o Windows 2000 o posterior</span><span class="sxs-lookup"><span data-stu-id="6a225-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="6a225-117">Versión de MIDL 3.1.76 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6a225-117">MIDL version 3.1.76 or later.</span></span>

 

 