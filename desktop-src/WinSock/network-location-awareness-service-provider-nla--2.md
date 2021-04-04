---
description: Los equipos personales que ejecutan Microsoft Windows suelen tener numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes, o una conexión de red física y una conexión de acceso telefónico.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Proveedor de servicios de reconocimiento de ubicación de red (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154259"
---
# <a name="network-location-awareness-service-provider-nla"></a><span data-ttu-id="33bfb-103">Proveedor de servicios de reconocimiento de ubicación de red (NLA)</span><span class="sxs-lookup"><span data-stu-id="33bfb-103">Network Location Awareness Service Provider (NLA)</span></span>

<span data-ttu-id="33bfb-104">Los equipos personales que ejecutan Microsoft Windows suelen tener numerosas conexiones de red, como varias tarjetas de interfaz de red (NIC) conectadas a redes diferentes, o una conexión de red física y una conexión de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="33bfb-104">Personal computers running Microsoft Windows often have numerous network connections, such as multiple network interface cards (NIC) connected to different networks, or a physical network connection and a dial-up connection.</span></span> <span data-ttu-id="33bfb-105">Windows Sockets es capaz de enumerar las interfaces de red disponibles durante algún tiempo, pero cierta información crítica sobre las conexiones de red no estaba disponible anteriormente.</span><span class="sxs-lookup"><span data-stu-id="33bfb-105">Windows Sockets has been capable of enumerating available network interfaces for some time, but certain critical information about network connections was previously unavailable.</span></span> <span data-ttu-id="33bfb-106">Esto incluye información como la red lógica a la que está conectado un equipo Windows o si varias interfaces están conectadas a la misma red.</span><span class="sxs-lookup"><span data-stu-id="33bfb-106">This includes information such as the logical network to which a Windows computer is attached or whether multiple interfaces are connected to the same network.</span></span>

<span data-ttu-id="33bfb-107">El proveedor de servicios de reconocimiento de ubicación de red, comúnmente conocido como NLA, permite que las aplicaciones de Windows Sockets 2 identifiquen la red lógica a la que está conectado un equipo Windows.</span><span class="sxs-lookup"><span data-stu-id="33bfb-107">The Network Location Awareness service provider, commonly referred to as NLA, enables Windows Sockets 2 applications to identify the logical network to which a Windows computer is attached.</span></span> <span data-ttu-id="33bfb-108">Además, NLA permite a las aplicaciones de Windows Sockets identificar en qué interfaz de red física una aplicación determinada ha guardado información específica.</span><span class="sxs-lookup"><span data-stu-id="33bfb-108">In addition, NLA enables Windows Sockets applications to identify to which physical network interface a given application has saved specific information.</span></span> <span data-ttu-id="33bfb-109">NLA se implementa como un proveedor de servicios de resolución de nombres genérico de Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="33bfb-109">NLA is implemented as a generic Windows Sockets 2 Name Resolution service provider.</span></span>

 

 



