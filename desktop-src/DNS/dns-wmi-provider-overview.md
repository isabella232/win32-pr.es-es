---
title: Introducción al proveedor WMI de DNS
description: Un proveedor es un elemento arquitectónico de Instrumental de administración de Windows (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Sistema de nombres de dominio, proveedor WMI, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075593"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="1dbf3-104">Introducción al proveedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="1dbf3-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="1dbf3-105">Un proveedor es un elemento arquitectónico de *instrumental de administración de Windows (WMI)*.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="1dbf3-106">WMI define una arquitectura unificada para describir, obtener acceso e instrumentar objetos.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="1dbf3-107">Parte de esta arquitectura es una base de datos grande de clases WMI que se usa para llevar a cabo tareas de administración remota en objetos específicos.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="1dbf3-108">Los proveedores de WMI actúan como intermediarios entre WMI y uno o varios objetos administrados.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="1dbf3-109">Cuando WMI recibe una solicitud de una aplicación de administración para datos que no están disponibles en el repositorio CIM o para notificaciones de eventos que WMI no admite, reenvía la solicitud a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="1dbf3-110">Los proveedores proporcionan datos y notificaciones de eventos para objetos administrados específicos de su dominio particular.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="1dbf3-111">Un proveedor extiende el esquema WMI de las clases para permitir que WMI funcione con nuevos tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="1dbf3-112">El proveedor WMI de DNS define las clases para consultar y configurar un servidor DNS, junto con sus registros DNS y zonas DNS asociados.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="1dbf3-113">El proveedor WMI de DNS expone una serie de objetos DNS a los clientes, incluido el servidor DNS, el dominio DNS y los objetos RR DNS.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="1dbf3-114">A través de estos objetos, los clientes pueden realizar actividades de administración de DNS.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="1dbf3-115">Con el proveedor WMI de DNS, puede crear sus propias herramientas para realizar la mayoría de las tareas de administración del servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="1dbf3-116">Por ejemplo, puede crear, eliminar y ver las zonas y los registros; restablecer las propiedades del servidor y de la zona; y realizan operaciones de administración rutinarias, como actualizar la zona, volver a cargar la zona, actualizar la zona, escribir la zona en un archivo o Active Directory, pausar y reanudar la zona, borrar la memoria caché, detener e iniciar el servicio DNS y ver las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="1dbf3-117">El proveedor WMI de DNS tiene un conjunto de comportamientos únicos que no se encuentran en otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="1dbf3-118">Vea la [Referencia del proveedor WMI de DNS](dns-wmi-provider-reference.md) para obtener información sobre la clase.</span><span class="sxs-lookup"><span data-stu-id="1dbf3-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 




