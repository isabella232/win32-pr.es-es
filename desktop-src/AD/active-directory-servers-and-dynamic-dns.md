---
title: Servidores de Active Directory y DNS dinámico
description: Los servidores Active Directory publican sus direcciones de modo que los clientes puedan encontrarlos sabiendo solo el nombre de dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dinámico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772757"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="e2a9f-104">Servidores de Active Directory y DNS dinámico</span><span class="sxs-lookup"><span data-stu-id="e2a9f-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="e2a9f-105">Los servidores Active Directory publican sus direcciones de modo que los clientes puedan encontrarlos sabiendo solo el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="e2a9f-106">Los servidores Active Directory se publican mediante los registros de recursos de servicio (RR de SRV) en DNS.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="e2a9f-107">SRV RR es un registro DNS que se usa para asignar el nombre de un servicio a la dirección de un servidor que ofrece el servicio.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="e2a9f-108">El nombre de un RR SRV tiene este formato:</span><span class="sxs-lookup"><span data-stu-id="e2a9f-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="e2a9f-109">Los servidores Active Directory ofrecen el servicio LDAP a través del protocolo TCP para que los nombres publicados sean "LDAP. TCP. <domain> ".</span><span class="sxs-lookup"><span data-stu-id="e2a9f-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="e2a9f-110">Por lo tanto, el RR SRV para fabrikam.com es "ldap.tcp.fabrikam.com".</span><span class="sxs-lookup"><span data-stu-id="e2a9f-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="e2a9f-111">Los datos adicionales sobre el RR SRV indican la prioridad y el peso del servidor, lo que permite a los clientes elegir el mejor servidor para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="e2a9f-112">Cuando se instala un servidor de Active Directory, utiliza DNS dinámico para publicarse.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="e2a9f-113">Dado que las direcciones TCP/IP están sujetas a cambios, los servidores comprueban periódicamente sus registros para asegurarse de que son correctos y los actualizan si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="e2a9f-114">DNS dinámico es una adición reciente al estándar DNS.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="e2a9f-115">DNS dinámico define un protocolo para actualizar dinámicamente un servidor DNS con nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="e2a9f-116">Antes del DNS dinámico, los administradores tenían que configurar manualmente los registros almacenados por los servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="e2a9f-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




