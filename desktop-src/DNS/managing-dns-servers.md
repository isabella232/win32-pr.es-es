---
title: Administración de servidores DNS
description: Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777964"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="a75cd-103">Administración de servidores DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-103">Managing DNS Servers</span></span>

<span data-ttu-id="a75cd-104">Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.</span><span class="sxs-lookup"><span data-stu-id="a75cd-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="a75cd-105">Los servidores DNS contienen archivos, denominados *archivos de zona*, que les permiten resolver nombres en direcciones IP (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="a75cd-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="a75cd-106">Cuando se consulta, un servidor DNS responde de una de estas tres maneras:</span><span class="sxs-lookup"><span data-stu-id="a75cd-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="a75cd-107">El servidor devuelve la información de resolución de nombres o resolución de IP solicitada.</span><span class="sxs-lookup"><span data-stu-id="a75cd-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="a75cd-108">El servidor devuelve un puntero a otro servidor DNS que puede atender la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a75cd-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="a75cd-109">El servidor indica que no tiene la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="a75cd-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="a75cd-110">Los servidores DNS podrían, durante el transcurso de la preparación de la devolución de la información de resolución solicitada, consultar otros servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="a75cd-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="a75cd-111">Pero más allá de eso, los servidores DNS no realizan ninguna operación distinta de la mencionada en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="a75cd-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="a75cd-112">Hay tres tipos principales de servidores DNS: los servidores principales, los servidores secundarios y los servidores de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="a75cd-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="a75cd-113">Consulte [servidores DNS](dns-servers.md) para obtener más información acerca de estos servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="a75cd-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="a75cd-114">Pasos de administración</span><span class="sxs-lookup"><span data-stu-id="a75cd-114">Administration Steps</span></span>

<span data-ttu-id="a75cd-115">El proveedor WMI de DNS permite la administración de servidores DNS desde el propio servidor o desde hosts remotos.</span><span class="sxs-lookup"><span data-stu-id="a75cd-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="a75cd-116">Los pasos generales necesarios para administrar un servidor DNS con el proveedor WMI de DNS son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a75cd-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="a75cd-117">Conexión al proveedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="a75cd-118">Obtener una instancia de servidor</span><span class="sxs-lookup"><span data-stu-id="a75cd-118">Getting a server instance</span></span>
-   <span data-ttu-id="a75cd-119">Enumerar o modificar una propiedad de servidor, o usar un método</span><span class="sxs-lookup"><span data-stu-id="a75cd-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="a75cd-120">Para ilustrar cómo implementar esos pasos de administración, se proporcionan ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a75cd-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="a75cd-121">Las siguientes tareas están vinculadas a sus ejemplos de scripting asociados.</span><span class="sxs-lookup"><span data-stu-id="a75cd-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="a75cd-122">Detención de un servidor DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-123">Inicio de un servidor DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-124">Reinicio de un servidor DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-125">Agregar una dirección IP</span><span class="sxs-lookup"><span data-stu-id="a75cd-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-126">Quitar una dirección IP</span><span class="sxs-lookup"><span data-stu-id="a75cd-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-127">Enumerar las propiedades del servidor DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-128">Mostrar tipos de propiedades de servidor DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a75cd-129">Modificación de las propiedades del servidor DNS</span><span class="sxs-lookup"><span data-stu-id="a75cd-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




