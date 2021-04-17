---
description: Instalación del servicio en el SPI de Windows Sockets 2 (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Instalación del servicio en Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696930"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="f35e5-103">Instalación del servicio en Windows Sockets 2 SPI</span><span class="sxs-lookup"><span data-stu-id="f35e5-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="f35e5-104">**NSPInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="f35e5-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="f35e5-105">**NSPRemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="f35e5-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="f35e5-106">**NSPSetService**</span><span class="sxs-lookup"><span data-stu-id="f35e5-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="f35e5-107">Cuando la clase de servicio necesaria todavía no existe, un cliente de espacio de nombres SPI usa [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) para instalar una nueva clase de servicio proporcionando un nombre de clase de servicio, un GUID para el identificador de clase de servicio y una serie de estructuras [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="f35e5-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="f35e5-108">Estas estructuras son específicas de un espacio de nombres determinado y proporcionan valores comunes, como los números de puerto TCP recomendados o los identificadores de SAP SAP.</span><span class="sxs-lookup"><span data-stu-id="f35e5-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="f35e5-109">Se puede quitar una clase de servicio llamando a [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) y proporcionando el GUID correspondiente al identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="f35e5-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="f35e5-110">Una vez que existe una clase de servicio, se pueden instalar o quitar instancias específicas de un servicio a través de [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span><span class="sxs-lookup"><span data-stu-id="f35e5-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="f35e5-111">Esta función toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como parámetro de entrada junto con un código de operación y marcas de operación.</span><span class="sxs-lookup"><span data-stu-id="f35e5-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="f35e5-112">El código de operación indica si el servicio se está instalando o quitando.</span><span class="sxs-lookup"><span data-stu-id="f35e5-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="f35e5-113">La estructura **WSAQUERYSET** proporciona toda la información relevante sobre el servicio, incluido el identificador de clase de servicio, el nombre de servicio (para esta instancia), la información del protocolo y el identificador de espacio de nombres aplicable, y un conjunto de direcciones de transporte en el que el servicio realiza escuchas.</span><span class="sxs-lookup"><span data-stu-id="f35e5-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 



