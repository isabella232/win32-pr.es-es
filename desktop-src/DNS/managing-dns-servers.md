---
title: Administración de servidores DNS
description: Obtenga información sobre la administración de servidores DNS. Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010779"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="c8466-104">Administración de servidores DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-104">Managing DNS Servers</span></span>

<span data-ttu-id="c8466-105">Un servidor DNS es un equipo que completa el proceso de resolución de nombres en DNS.</span><span class="sxs-lookup"><span data-stu-id="c8466-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="c8466-106">Los servidores DNS contienen archivos, denominados *archivos de zona,* que les permiten resolver nombres en direcciones IP (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="c8466-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="c8466-107">Cuando se consulta, un servidor DNS responde de una de estas tres maneras:</span><span class="sxs-lookup"><span data-stu-id="c8466-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="c8466-108">El servidor devuelve la información de resolución de nombres o resolución IP solicitada.</span><span class="sxs-lookup"><span data-stu-id="c8466-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="c8466-109">El servidor devuelve un puntero a otro servidor DNS que puede dar servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8466-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="c8466-110">El servidor indica que no tiene la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="c8466-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="c8466-111">Durante la preparación de la preparación para devolver la información de resolución solicitada, los servidores DNS podrían consultar otros servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="c8466-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="c8466-112">Pero más allá de eso, los servidores DNS no realizan ninguna operación que no sea la mencionada en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="c8466-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="c8466-113">Hay tres tipos principales de servidores DNS: servidores principales, servidores secundarios y servidores de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="c8466-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="c8466-114">Consulte [Servidores DNS para](dns-servers.md) obtener más información sobre estos servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="c8466-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="c8466-115">Pasos de administración</span><span class="sxs-lookup"><span data-stu-id="c8466-115">Administration Steps</span></span>

<span data-ttu-id="c8466-116">El proveedor WMI de DNS permite la administración de servidores DNS desde el propio servidor o desde hosts remotos.</span><span class="sxs-lookup"><span data-stu-id="c8466-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="c8466-117">Los pasos generales necesarios para administrar un servidor DNS mediante el proveedor WMI de DNS son:</span><span class="sxs-lookup"><span data-stu-id="c8466-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="c8466-118">Conexión al proveedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="c8466-119">Obtención de una instancia de servidor</span><span class="sxs-lookup"><span data-stu-id="c8466-119">Getting a server instance</span></span>
-   <span data-ttu-id="c8466-120">Enumerar o modificar una propiedad de servidor o usar un método</span><span class="sxs-lookup"><span data-stu-id="c8466-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="c8466-121">Para ilustrar cómo implementar esos pasos de administración, se proporcionan ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c8466-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="c8466-122">Las tareas siguientes están vinculadas a sus ejemplos de scripting asociados.</span><span class="sxs-lookup"><span data-stu-id="c8466-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="c8466-123">Detención de un servidor DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-124">Iniciar un servidor DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-125">Reiniciar un servidor DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-126">Adición de una dirección IP</span><span class="sxs-lookup"><span data-stu-id="c8466-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-127">Eliminación de una dirección IP</span><span class="sxs-lookup"><span data-stu-id="c8466-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-128">Enumeración de las propiedades del servidor DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-129">Mostrar tipos de propiedades de servidor DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="c8466-130">Modificar las propiedades del servidor DNS</span><span class="sxs-lookup"><span data-stu-id="c8466-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




