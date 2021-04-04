---
description: El orden en que se instalan inicialmente los proveedores de servicios de transporte rige el orden en que se enumeran a través de WSCEnumProtocols y WSCEnumProtocols32 en la interfaz del proveedor de servicios o a través de WSAEnumProtocols en la interfaz de la aplicación. Lo que es más importante, este orden también rige el orden en el que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, el tipo y el identificador de protocolo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordenación del proveedor de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908571"
---
# <a name="service-provider-ordering"></a><span data-ttu-id="4d9ff-104">Ordenación del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="4d9ff-104">Service Provider Ordering</span></span>

<span data-ttu-id="4d9ff-105">El orden en que se instalan inicialmente los proveedores de servicios de transporte rige el orden en que se enumeran a través de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) y [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) en la interfaz del proveedor de servicios o a través de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) en la interfaz de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-105">The order in which transport service providers are initially installed governs the order in which they are enumerated through [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) and [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) at the service provider interface, or through [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) at the application interface.</span></span> <span data-ttu-id="4d9ff-106">Lo que es más importante, este orden también rige el orden en el que se tienen en cuenta los protocolos y los proveedores de servicios cuando un cliente solicita la creación de un socket en función de su familia de direcciones, el tipo y el identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-106">More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.</span></span>

<span data-ttu-id="4d9ff-107">Windows Sockets 2 incluye un applet denominado Sporder.exe que permite que el catálogo de protocolos instalados se reordene de forma interactiva una vez que ya se hayan instalado los protocolos.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-107">Windows Sockets 2 includes an applet called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed.</span></span> <span data-ttu-id="4d9ff-108">Winsock también incluye un archivo DLL auxiliar, Sporder.dll, que exporta una interfaz de procedimientos para la reordenación de protocolos.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-108">Winsock also includes an auxiliary DLL, Sporder.dll, that exports a procedural interface for reordering protocols.</span></span> <span data-ttu-id="4d9ff-109">Esta interfaz de procedimientos consta de un único procedimiento denominado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span><span class="sxs-lookup"><span data-stu-id="4d9ff-109">This procedural interface consists of a single procedure called [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span></span>

<span data-ttu-id="4d9ff-110">La definición de la interfaz se puede importar en un programa de C o C++ por medio del archivo de inclusión sporder. h.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-110">The interface definition may be imported into a C or C++ program by means of the include file Sporder.h.</span></span> <span data-ttu-id="4d9ff-111">El punto de entrada puede estar vinculado por medio del archivo lib sporder. lib.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-111">The entry point may be linked by means of the lib file Sporder.lib.</span></span>

 

 



