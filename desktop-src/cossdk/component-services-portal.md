---
description: Extiende las aplicaciones escritas mediante tecnologías basadas en COM.
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: COM+ (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000570"
---
# <a name="com-component-services"></a><span data-ttu-id="52876-103">COM+ (servicios de componentes)</span><span class="sxs-lookup"><span data-stu-id="52876-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="52876-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="52876-104">Purpose</span></span>

<span data-ttu-id="52876-105">COM+ es una evolución del modelo de objetos componentes (COM) de Microsoft y de Microsoft Transaction Server (MTS).</span><span class="sxs-lookup"><span data-stu-id="52876-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="52876-106">COM+ se basa en y extiende las aplicaciones escritas mediante COM, MTS y otras tecnologías basadas en COM.</span><span class="sxs-lookup"><span data-stu-id="52876-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="52876-107">COM+ controla muchas de las tareas de administración de recursos que tenía antes de programar, como la asignación de subprocesos y la seguridad.</span><span class="sxs-lookup"><span data-stu-id="52876-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="52876-108">COM+ también hace que las aplicaciones sean más escalables proporcionando agrupación de subprocesos, agrupación de objetos y activación de objetos Just-in-Time.</span><span class="sxs-lookup"><span data-stu-id="52876-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="52876-109">COM+ también ayuda a proteger la integridad de los datos al proporcionar compatibilidad con las transacciones, incluso si una transacción abarca varias bases de datos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="52876-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="52876-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="52876-110">Where applicable</span></span>

<span data-ttu-id="52876-111">COM+ se puede usar para desarrollar aplicaciones distribuidas críticas para la empresa para Windows.</span><span class="sxs-lookup"><span data-stu-id="52876-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="52876-112">Si es administrador del sistema, instalará, implementará y configurará las aplicaciones COM+ y sus componentes.</span><span class="sxs-lookup"><span data-stu-id="52876-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="52876-113">Si es un programador de aplicaciones, escribirá componentes y los integrará como aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="52876-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="52876-114">Si es un proveedor de herramientas, va a desarrollar o modificar herramientas para que funcionen en el entorno de COM+.</span><span class="sxs-lookup"><span data-stu-id="52876-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="52876-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="52876-115">Developer audience</span></span>

<span data-ttu-id="52876-116">COM+ está diseñado principalmente para los desarrolladores de Microsoft Visual C++ y Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="52876-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="52876-117">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="52876-117">Run-time requirements</span></span>

<span data-ttu-id="52876-118">La versión 1,5 de COM+ se incluye en Windows a partir de Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="52876-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="52876-119">La versión 1,0 de COM+ se incluye en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="52876-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="52876-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="52876-120">In this section</span></span>

-   [<span data-ttu-id="52876-121">Novedades de COM+ 1,5</span><span class="sxs-lookup"><span data-stu-id="52876-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="52876-122">Información general sobre desarrolladores de COM+</span><span class="sxs-lookup"><span data-stu-id="52876-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="52876-123">Servicios COM+</span><span class="sxs-lookup"><span data-stu-id="52876-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="52876-124">Tareas generales de COM+</span><span class="sxs-lookup"><span data-stu-id="52876-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="52876-125">Referencia de COM+</span><span class="sxs-lookup"><span data-stu-id="52876-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="52876-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52876-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52876-127">COM</span><span class="sxs-lookup"><span data-stu-id="52876-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
