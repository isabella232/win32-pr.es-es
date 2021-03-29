---
title: Nombres de host y direcciones IP
description: Las redes TCP/IP requieren que los nombres de host se resuelvan en direcciones IP antes de que se pueda usar la información de la dirección para crear una conexión.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Nombres de host y direcciones IP SNMP
- Nombres de host, resolver SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775115"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="77b33-105">Nombres de host y direcciones IP</span><span class="sxs-lookup"><span data-stu-id="77b33-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="77b33-106">Las redes TCP/IP requieren que los nombres de host se resuelvan en direcciones IP antes de que se pueda usar la información de la dirección para crear una conexión.</span><span class="sxs-lookup"><span data-stu-id="77b33-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="77b33-107">Los equipos que se ejecutan en el sistema operativo Windows usan un archivo host que, para este propósito, asigna los nombres de host a las direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="77b33-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="77b33-108">El archivo host es un archivo de texto que muestra los nombres de host y las direcciones IP explícitos.</span><span class="sxs-lookup"><span data-stu-id="77b33-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="77b33-109">El archivo host se carga automáticamente en la memoria en el inicio y se consulta cuando un nombre de host requiere resolución.</span><span class="sxs-lookup"><span data-stu-id="77b33-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="77b33-110">Si el archivo host no contiene la información de asignación necesaria para resolver un nombre de host específico en su dirección IP, se realiza una consulta de resolución en un servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="77b33-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="77b33-111">SNMP utiliza el Naming Service de Internet de Windows (WINS) para la resolución de nombres de host.</span><span class="sxs-lookup"><span data-stu-id="77b33-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="77b33-112">WINS hace posible asignar nombres NetBIOS o nombres de equipo a direcciones IP en redes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="77b33-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="77b33-113">Si el equipo no puede tener acceso a un servidor WINS, el servicio SNMP utiliza el archivo host para resolver nombres de host en direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="77b33-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="77b33-114">El servicio SNMP admite el uso de los nombres de host y las direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="77b33-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="77b33-115">Sin embargo, si tiene la opción de usar nombres de host o direcciones IP para identificar ubicaciones de red, las aplicaciones de administración SNMP deben usar nombres de host.</span><span class="sxs-lookup"><span data-stu-id="77b33-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="77b33-116">Si usa nombres de host, agregue todas las asignaciones de nombre de host y dirección IP de los sistemas participantes al archivo host.</span><span class="sxs-lookup"><span data-stu-id="77b33-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




