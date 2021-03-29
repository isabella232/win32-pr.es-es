---
title: El rol de administrador de lista de redes
description: El rol de administrador de lista de redes
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903872"
---
# <a name="the-role-of-network-list-manager"></a><span data-ttu-id="c7753-103">El rol de administrador de lista de redes</span><span class="sxs-lookup"><span data-stu-id="c7753-103">The Role of Network List Manager</span></span>

<span data-ttu-id="c7753-104">Antes de Windows XP y Windows Server 2003, las aplicaciones tenían que llamar a varias API no relacionadas para obtener datos acerca de los atributos de red, como la dirección IP, el controlador de dominio o el sistema de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="c7753-104">Prior to Windows XP and Windows Server 2003, applications were required to call a number of unrelated APIs to obtain data about network attributes such as the IP address, the domain controller, or the Domain Name System (DNS).</span></span> <span data-ttu-id="c7753-105">A partir de Windows XP y Windows Server 2003, la API de reconocimiento de ubicación de red de Winsock incluye un conjunto limitado de funciones de ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="c7753-105">Starting with Windows XP and Windows Server 2003, the Network Location Awareness Winsock API featured a limited set of network location functionality.</span></span> <span data-ttu-id="c7753-106">En Windows Server 2008 y Windows Vista, el servicio de reconocimiento de redes captura los atributos de red en una ubicación y permite que las aplicaciones consulten y recuperen redes y atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="c7753-106">In Windows Server 2008 and Windows Vista, the Network Awareness service captures the network attributes in one location and allows applications to query and retrieve specific networks and attributes.</span></span> <span data-ttu-id="c7753-107">El administrador de listas de redes reemplaza la funcionalidad de la API de Winsock anterior (disponible como proveedor de espacio de nombres de Winsock) al tiempo que mantiene la compatibilidad con aplicaciones anteriores mediante la API de Winsock.</span><span class="sxs-lookup"><span data-stu-id="c7753-107">Network List Manager replaces the functionality of the previous Winsock API (available as a Winsock Name Space Provider) while maintaining compatibility with older applications using the Winsock API.</span></span>

 

 




