---
description: Modelo de registro y resolución de nombres para el SPI de Windows Sockets (Winsock).
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modelo de resolución de nombres para SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154262"
---
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="ee1f6-103">Modelo de resolución de nombres para SPI</span><span class="sxs-lookup"><span data-stu-id="ee1f6-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="ee1f6-104">En el desarrollo de una aplicación cliente/servidor independiente del Protocolo, existen dos requisitos básicos con respecto a la resolución de nombres y el registro:</span><span class="sxs-lookup"><span data-stu-id="ee1f6-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="ee1f6-105">La capacidad de la mitad del servidor de la aplicación (a la que se hace referencia como servicio) para registrar su existencia en uno o varios espacios de nombres (o ser accesibles).</span><span class="sxs-lookup"><span data-stu-id="ee1f6-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="ee1f6-106">La capacidad de la aplicación cliente de buscar el servicio dentro de un espacio de nombres y obtener el protocolo de transporte y la información de direccionamiento necesarios.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="ee1f6-107">Para aquellos que están acostumbrados a desarrollar aplicaciones basadas en TCP/IP, esto puede suponer un poco más que buscar una dirección de host y, a continuación, usar un número de Puerto acordado.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="ee1f6-108">Otros esquemas de red, sin embargo, permiten la ubicación del servicio, el protocolo usado para el servicio y otros atributos que se detectan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="ee1f6-109">Para acomodar el intervalo de capacidades que se encuentran en los servicios de nombres existentes, la interfaz de Windows Sockets 2 adopta el modelo que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="ee1f6-110">Un *espacio de nombres* hace referencia a alguna funcionalidad para asociar (como mínimo) el protocolo y el direccionamiento de los atributos de un servicio de red con uno o más nombres descriptivos.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="ee1f6-111">Muchos espacios de nombres están actualmente en uso amplio, incluidos el sistema de nombres de dominio (DNS) de Internet, Servicios de directorio NetWare (NDS), X. 500, etc. Estos espacios de nombres varían considerablemente en el modo en que se organizan e implementan.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="ee1f6-112">Algunas de sus propiedades son especialmente importantes para comprender desde la perspectiva de la resolución de nombres de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="ee1f6-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



