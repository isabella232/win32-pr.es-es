---
description: El proveedor de servicios de reconocimiento de ubicación de red (NLA) es fundamental para equipos o dispositivos que pueden moverse entre distintas redes y para seleccionar configuraciones óptimas cuando hay más de una disponible.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: El rol de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276269"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="0b9dd-103">El rol de NLA</span><span class="sxs-lookup"><span data-stu-id="0b9dd-103">The Role of NLA</span></span>

<span data-ttu-id="0b9dd-104">El proveedor de servicios de reconocimiento de ubicación de red (NLA) es fundamental para equipos o dispositivos que pueden moverse entre distintas redes y para seleccionar configuraciones óptimas cuando hay más de una disponible.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="0b9dd-105">Por ejemplo, un equipo inalámbrico que se itinerancia entre redes físicas puede usar NLA para determinar la configuración adecuada en función de la información sobre la conexión de red disponible.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="0b9dd-106">NLA también resulta útil cuando un equipo de host múltiple tiene una conexión física a una red mientras también está conectado a otra red a través de una conexión de acceso telefónico o un túnel.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="0b9dd-107">En el pasado, los desarrolladores tenían que obtener información sobre una interfaz de red lógica y, por lo tanto, tomar decisiones sobre la conectividad de red, en función de una gran cantidad de información de red dispares.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="0b9dd-108">En esas circunstancias, los desarrolladores tenían que elegir la interfaz de red adecuada en función de la dirección IP, la subred de la interfaz, el nombre del sistema de nombres de dominio (DNS) asociado a la interfaz, la dirección MAC de una NIC, un nombre de red inalámbrica u otra información de red.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="0b9dd-109">NLA reduce este problema proporcionando una interfaz estándar para enumerar la información de los datos adjuntos de la red lógica, correlacionarla con la información de la interfaz de red física y, a continuación, proporcionar una notificación cuando se invalida la información devuelta previamente.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="0b9dd-110">NLA proporciona la siguiente información de ubicación de red:</span><span class="sxs-lookup"><span data-stu-id="0b9dd-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="0b9dd-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identidad de red lógica</span><span class="sxs-lookup"><span data-stu-id="0b9dd-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="0b9dd-112">NLA primero intenta identificar una red lógica por su nombre de dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="0b9dd-113">Si una red lógica no tiene un nombre de dominio, NLA identifica la red a partir de la información estática personalizada almacenada en el registro y, por último, de su dirección de subred.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="0b9dd-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces de red lógica</span><span class="sxs-lookup"><span data-stu-id="0b9dd-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="0b9dd-115">Para cada red a la que está conectado un equipo, NLA proporciona un *AdapterName* que identifica de forma única una interfaz física como una NIC o una interfaz lógica como una conexión RAS.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="0b9dd-116">A continuación, AdapterName se puede usar con las funciones disponibles en la API auxiliar de IP para obtener más características de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="0b9dd-117">NLA implementa la red lógica como una clase de servicio, con una propiedad y un GUID de clase asociados.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="0b9dd-118">Cada red lógica para la que NLA devuelve información es una instancia de esa clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="0b9dd-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



