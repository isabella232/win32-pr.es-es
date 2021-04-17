---
title: La base de datos del servicio de nombres RPC
description: Un servicio de nombres es un servicio que asigna nombres a objetos y normalmente mantiene los pares (nombre, objeto) en una base de datos.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Llamada a procedimiento remoto RPC, descripción, nombre base de datos de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486874"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="35325-104">La base de datos del servicio de nombres RPC</span><span class="sxs-lookup"><span data-stu-id="35325-104">The RPC Name Service Database</span></span>

<span data-ttu-id="35325-105">Un servicio de nombres es un servicio que asigna nombres a objetos y normalmente mantiene los pares (nombre, objeto) en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="35325-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="35325-106">Por lo general, el nombre es un nombre lógico que es fácil de recordar para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="35325-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="35325-107">Por ejemplo, un servicio de nombres permitiría que un usuario utilizara el nombre lógico "laserprinter".</span><span class="sxs-lookup"><span data-stu-id="35325-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="35325-108">El servicio de nombres asigna este nombre al nombre específico de la red que usa el servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="35325-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="35325-109">Para usar una explicación simplificada, el servicio de nombres RPC asigna un nombre a un identificador de enlace y mantiene las asignaciones (nombre, identificador de enlace) en la base de datos del servicio de nombres de RPC.</span><span class="sxs-lookup"><span data-stu-id="35325-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="35325-110">El servicio de nombres RPC permite a las aplicaciones cliente utilizar un nombre lógico en lugar de una secuencia de protocolo y una dirección de red específicas.</span><span class="sxs-lookup"><span data-stu-id="35325-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="35325-111">El uso del nombre lógico facilita a los administradores de red la instalación y configuración de la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="35325-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="35325-112">Una entrada de base de datos del servicio de nombres RPC tiene uno de los siguientes atributos: **servidor**, **Grupo** o **perfil**.</span><span class="sxs-lookup"><span data-stu-id="35325-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="35325-113">En la implementación de Microsoft, las entradas solo pueden tener un atributo, por lo que estas entradas también se conocen como entradas de servidor, entradas de grupo y entradas de perfil.</span><span class="sxs-lookup"><span data-stu-id="35325-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="35325-114">La entrada del servidor consiste en la interfaz UUID, el objeto UUID (necesario cuando el servidor implementa puntos de entrada múltiples), la dirección de red, la secuencia de protocolo y cualquier información de punto de conexión asociada con puntos de conexión conocidos.</span><span class="sxs-lookup"><span data-stu-id="35325-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="35325-115">Cuando se usa un punto de conexión dinámico, la información del punto de conexión se mantiene en la base de datos de asignación de extremos en lugar de en la base de datos del servicio de nombres y el punto de conexión se resuelve como cualquier otro punto de conexión dinámico.</span><span class="sxs-lookup"><span data-stu-id="35325-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="35325-116">Las entradas del servidor se administran mediante funciones que comienzan con el prefijo "RpcNsBinding".</span><span class="sxs-lookup"><span data-stu-id="35325-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="35325-117">La entrada de grupo puede contener entradas de servidor u otras entradas de grupo.</span><span class="sxs-lookup"><span data-stu-id="35325-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="35325-118">Las entradas de grupo se administran mediante funciones que comienzan con el prefijo "RpcNsGroup".</span><span class="sxs-lookup"><span data-stu-id="35325-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="35325-119">La entrada de perfil puede contener entradas de perfil, de grupo o de servidor.</span><span class="sxs-lookup"><span data-stu-id="35325-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="35325-120">Las funciones que empiezan por el prefijo "RpcNsProfile" administran las entradas de perfil.</span><span class="sxs-lookup"><span data-stu-id="35325-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="35325-121">En esta sección se presenta una introducción a la base de datos del servicio de nombres en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="35325-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="35325-122">Instrucciones de aplicación de servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="35325-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="35325-123">Información general de la entrada del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="35325-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="35325-124">Criterios para las entradas del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="35325-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="35325-125">Limpieza de entradas del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="35325-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="35325-126">Lo que sucede durante una consulta</span><span class="sxs-lookup"><span data-stu-id="35325-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="35325-127">Uso del localizador de Microsoft</span><span class="sxs-lookup"><span data-stu-id="35325-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="35325-128">Uso del Servicio de directorio de celdas (CDS)</span><span class="sxs-lookup"><span data-stu-id="35325-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="35325-129">Sintaxis de nombre</span><span class="sxs-lookup"><span data-stu-id="35325-129">Name Syntax</span></span>](name-syntax.md)

 

 




