---
description: La API de agrupación del mismo nivel combina la tecnología de la API de proveedor de espacio de nombres PNRP y la API de gráficos.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Acerca de la API de agrupación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667464"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="276c2-103">Acerca de la API de agrupación</span><span class="sxs-lookup"><span data-stu-id="276c2-103">About the Grouping API</span></span>

<span data-ttu-id="276c2-104">La API de agrupación del mismo nivel combina la tecnología de la [API de proveedor de espacio de nombres PNRP](pnrp-namespace-provider-api.md) y la [API de gráficos](graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="276c2-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="276c2-105">La agrupación agrega los dos siguientes elementos de tecnología:</span><span class="sxs-lookup"><span data-stu-id="276c2-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="276c2-106">Capa de multiplexación que permite que varias aplicaciones utilicen un gráfico, un puerto y una base de datos de registros.</span><span class="sxs-lookup"><span data-stu-id="276c2-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="276c2-107">Seguridad que garantiza que solo los elementos del mismo nivel invitados a un grupo pueden unirse y conectarse a lo largo de la duración de un grupo.</span><span class="sxs-lookup"><span data-stu-id="276c2-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="276c2-108">La agrupación proporciona un enfoque accesible y sencillo a las redes del mismo nivel debido al flujo de llamadas sencillo y a la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="276c2-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="276c2-109">Esta API emplea PNRP para la detección de grupos y un proveedor de seguridad basado en PKI estándar en lugar de requerir a un desarrollador que implemente uno.</span><span class="sxs-lookup"><span data-stu-id="276c2-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="276c2-110">Sin embargo, si la aplicación exige una mayor flexibilidad en términos de opciones de seguridad, considere la posibilidad de usar la [API de gráficos](about-the-graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="276c2-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="276c2-111">En la tabla siguiente se identifican los temas de esta sección de la API de agrupación:</span><span class="sxs-lookup"><span data-stu-id="276c2-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="276c2-112">Tema</span><span class="sxs-lookup"><span data-stu-id="276c2-112">Topic</span></span>                                                                | <span data-ttu-id="276c2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="276c2-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="276c2-114">Cómo trabajar con grupos</span><span class="sxs-lookup"><span data-stu-id="276c2-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="276c2-115">Describe el flujo de llamadas en una aplicación de agrupación del mismo nivel desde el inicio hasta el apagado.</span><span class="sxs-lookup"><span data-stu-id="276c2-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="276c2-116">Cómo funciona la seguridad de grupo</span><span class="sxs-lookup"><span data-stu-id="276c2-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="276c2-117">Describe cómo se protege la pertenencia a grupos del mismo nivel y los intercambios de datos.</span><span class="sxs-lookup"><span data-stu-id="276c2-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="276c2-118">Invitar a un elemento del mismo nivel a un grupo</span><span class="sxs-lookup"><span data-stu-id="276c2-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="276c2-119">Describe el proceso por el que se invita a los elementos del mismo nivel y se agregan a un grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="276c2-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="276c2-120">Cómo conectarse a un grupo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="276c2-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="276c2-121">Describe cómo un elemento del mismo nivel se conecta e interactúa con un grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="276c2-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="276c2-122">Administrar registros de grupo</span><span class="sxs-lookup"><span data-stu-id="276c2-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="276c2-123">Describe los registros de grupo del mismo nivel y cómo administrarlos como miembro y como administrador.</span><span class="sxs-lookup"><span data-stu-id="276c2-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="276c2-124">Las aplicaciones que usan la API de agrupación en un entorno con un firewall requieren grupos de excepciones que cubran el puerto específico de la aplicación, así como el puerto ' 3587-TCP ' para la API de agrupación y el puerto ' 3540-UDP ' para PNRP.</span><span class="sxs-lookup"><span data-stu-id="276c2-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="276c2-125">Estos grupos de excepciones se deben habilitar cada vez que se ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="276c2-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



