---
description: Resolución de nombres independiente del protocolo y Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Resolución de nombres de Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360294"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="c0e37-103">Resolución de nombres de Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="c0e37-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="c0e37-104">En el desarrollo de una aplicación cliente/servidor independiente del Protocolo, existen dos requisitos básicos con respecto a la resolución de nombres y el registro:</span><span class="sxs-lookup"><span data-stu-id="c0e37-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="c0e37-105">La capacidad de la mitad del servidor de la aplicación (servicio) de registrar su existencia en uno o varios espacios de nombres (o se puede tener acceso a ellos).</span><span class="sxs-lookup"><span data-stu-id="c0e37-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="c0e37-106">La capacidad de la aplicación cliente de buscar el servicio dentro de un espacio de nombres y obtener el protocolo de transporte y la información de direccionamiento necesarios.</span><span class="sxs-lookup"><span data-stu-id="c0e37-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="c0e37-107">En el caso de los usuarios acostumbrados a desarrollar aplicaciones basadas en TCP/IP, esto puede parecer un poco más que buscar una dirección de host y, a continuación, usar un número de Puerto acordado.</span><span class="sxs-lookup"><span data-stu-id="c0e37-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="c0e37-108">Sin embargo, otros esquemas de red permiten la ubicación del servicio, el protocolo usado para el servicio y otros atributos que se detectan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c0e37-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="c0e37-109">Para dar cabida a la amplia diversidad de capacidades que se encuentran en los servicios de nombres existentes, la interfaz de Windows Sockets 2 adopta el modelo descrito en los temas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="c0e37-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="c0e37-110">En esta sección se describen las capacidades de resolución de nombres independientes del protocolo disponibles para los desarrolladores de Winsock.</span><span class="sxs-lookup"><span data-stu-id="c0e37-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="c0e37-111">En la lista siguiente se describen los temas de esta sección:</span><span class="sxs-lookup"><span data-stu-id="c0e37-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="c0e37-112">Modelo de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c0e37-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="c0e37-113">Resumen de las funciones de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c0e37-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="c0e37-114">Estructuras de datos de resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c0e37-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="c0e37-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0e37-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0e37-116">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c0e37-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



