---
title: API WinSNMP
description: Las versiones 1.1 a y 2,0 de la interfaz de programación de aplicaciones (API WinSNMP) de Microsoft Windows SNMP permiten desarrollar aplicaciones de administración de red basadas en SNMP que se ejecutan en el entorno de Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078087"
---
# <a name="winsnmp-api"></a><span data-ttu-id="dc124-104">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-104">WinSNMP API</span></span>

<span data-ttu-id="dc124-105">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="dc124-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dc124-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="dc124-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="dc124-107">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="dc124-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="dc124-108">Las versiones 1.1 a y 2,0 de la interfaz de programación de aplicaciones (API WinSNMP) de Microsoft Windows SNMP permiten desarrollar aplicaciones de administración de red basadas en SNMP que se ejecutan en el entorno de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc124-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="dc124-109">El Protocolo simple de administración de redes (SNMP) es un protocolo de solicitud-respuesta que transfiere información de administración entre las entidades del protocolo.</span><span class="sxs-lookup"><span data-stu-id="dc124-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="dc124-110">WinSNMP se ha desarrollado conjuntamente con la cooperación, la entrada y el soporte técnico de varias empresas, asociaciones y usuarios.</span><span class="sxs-lookup"><span data-stu-id="dc124-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="dc124-111">En la primera parte de esta información general se proporciona información sobre el anexo WinSNMP 2,0, las versiones de SNMP y una lista de las solicitudes de comentarios (RFC) pertinentes.</span><span class="sxs-lookup"><span data-stu-id="dc124-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="dc124-112">También se describe el modelo WinSNMP y los componentes y características de la implementación de Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="dc124-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="dc124-113">También proporciona información sobre la administración de datos y los conceptos de comunicaciones que debe programar en el entorno WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="dc124-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="dc124-114">En la segunda sección se describen las funciones WinSNMP y las siguientes tareas de programación WinSNMP relacionadas:</span><span class="sxs-lookup"><span data-stu-id="dc124-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="dc124-115">Abrir y cerrar una aplicación WinSNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="dc124-116">Abrir y cerrar una sesión WinSNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="dc124-117">Administración de capturas y notificaciones</span><span class="sxs-lookup"><span data-stu-id="dc124-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="dc124-118">Trabajar con listas de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="dc124-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="dc124-119">Trabajar con unidades de datos de protocolo</span><span class="sxs-lookup"><span data-stu-id="dc124-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="dc124-120">Envío de mensajes SNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="dc124-121">Recepción de mensajes SNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="dc124-122">Administrar identificadores de objeto</span><span class="sxs-lookup"><span data-stu-id="dc124-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="dc124-123">Liberación de descriptores WinSNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="dc124-124">Establecer el modo de traducción de entidad y contexto</span><span class="sxs-lookup"><span data-stu-id="dc124-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="dc124-125">Administrar la Directiva de retransmisión</span><span class="sxs-lookup"><span data-stu-id="dc124-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="dc124-126">Escribir aplicaciones WinSNMP con varios subprocesos</span><span class="sxs-lookup"><span data-stu-id="dc124-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="dc124-127">Registro de una aplicación de agente SNMP</span><span class="sxs-lookup"><span data-stu-id="dc124-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="dc124-128">Antes de leer esta información general, debe estar familiarizado con los conceptos básicos de la programación de SNMP y Windows.</span><span class="sxs-lookup"><span data-stu-id="dc124-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="dc124-129">Para obtener más información acerca de SNMP, consulte [Protocolo simple de administración de redes](simple-network-management-protocol-snmp-.md) y las solicitudes de comentarios (RFC) relevantes publicadas por Internet Engineering Task Force (IETF).</span><span class="sxs-lookup"><span data-stu-id="dc124-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 