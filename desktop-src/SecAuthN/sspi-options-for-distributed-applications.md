---
description: Opciones de SSPI para aplicaciones distribuidas
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opciones de SSPI para aplicaciones distribuidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907607"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="74a92-103">Opciones de SSPI para aplicaciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="74a92-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="74a92-104">Los desarrolladores tienen muchas opciones para compilar aplicaciones distribuidas.</span><span class="sxs-lookup"><span data-stu-id="74a92-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="74a92-105">La [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) proporciona una capa de abstracción entre los protocolos de nivel de aplicación y los [*protocolos de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="74a92-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="74a92-106">Las aplicaciones pueden aprovechar los protocolos de seguridad SSPI de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="74a92-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="74a92-107">Llamar a rutinas SSPI directamente (para aplicaciones tradicionales basadas en socket).</span><span class="sxs-lookup"><span data-stu-id="74a92-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="74a92-108">Las rutinas usan mensajes de solicitud/respuesta para implementar el [*Protocolo de aplicación*](../secgloss/a-gly.md) que transporta los datos relacionados con la seguridad de SSPI.</span><span class="sxs-lookup"><span data-stu-id="74a92-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="74a92-109">Use COM para llamar a las opciones de seguridad que se implementan mediante RPC autenticado y SSPI en niveles inferiores.</span><span class="sxs-lookup"><span data-stu-id="74a92-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="74a92-110">Estas aplicaciones no llaman directamente a las funciones SSPI.</span><span class="sxs-lookup"><span data-stu-id="74a92-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="74a92-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) con la interfaz Winsock extendida para permitir que los proveedores de transporte utilicen las características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="74a92-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="74a92-112">Este enfoque integra el [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) en la pila de red y proporciona servicios de transporte y seguridad a través de una interfaz común.</span><span class="sxs-lookup"><span data-stu-id="74a92-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="74a92-113">Use la [API de extensiones de Internet de Windows](../wininet/portal.md) (WinInet) y una interfaz diseñada para admitir protocolos de seguridad de Internet como el protocolo [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL).</span><span class="sxs-lookup"><span data-stu-id="74a92-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="74a92-114">Las aplicaciones usan la interfaz SSPI en el proveedor de seguridad de [canal seguro](secure-channel.md) (Schannel) para implementar la seguridad de Wininet.</span><span class="sxs-lookup"><span data-stu-id="74a92-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="74a92-115">Schannel es la implementación de Microsoft de SSL.</span><span class="sxs-lookup"><span data-stu-id="74a92-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="74a92-116">Varias funciones SSPI devuelven marcas de tiempo que representan la duración de varios objetos.</span><span class="sxs-lookup"><span data-stu-id="74a92-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="74a92-117">Los [*paquetes de seguridad*](../secgloss/s-gly.md) pueden mantener el tiempo y proporcionar marcas de tiempo de maneras diferentes, pero el uso de la hora local simplifica el trabajo de las aplicaciones que usan funciones SSPI.</span><span class="sxs-lookup"><span data-stu-id="74a92-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 
