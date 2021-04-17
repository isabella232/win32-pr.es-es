---
description: Una aplicación que contiene al menos un componente queuable se puede marcar como en cola mediante la herramienta administrativa Servicios de componentes.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Crear colas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705305"
---
# <a name="creating-component-queues"></a><span data-ttu-id="08e65-103">Crear colas de componentes</span><span class="sxs-lookup"><span data-stu-id="08e65-103">Creating Component Queues</span></span>

<span data-ttu-id="08e65-104">Una aplicación que contiene al menos un componente queuable se puede marcar como en cola mediante la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="08e65-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="08e65-105">Cuando una aplicación se marca como en cola, COM+ crea automáticamente una cola de Message Queue Server para ella.</span><span class="sxs-lookup"><span data-stu-id="08e65-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="08e65-106">El nombre de la cola es el nombre de la aplicación; Si el nombre de la cola coincide con el nombre de una cola existente, COM+ usará la cola existente.</span><span class="sxs-lookup"><span data-stu-id="08e65-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="08e65-107">El parámetro *PathName* de Message Queue Server es una combinación del nombre del servidor remoto (RSN) y el nombre de la aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="08e65-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="08e65-108">El RSN hace referencia al destino de una activación remota.</span><span class="sxs-lookup"><span data-stu-id="08e65-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="08e65-109">El RSN se especifica durante la instalación de una aplicación exportable de cliente en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="08e65-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="08e65-110">El procedimiento de instalación utiliza el RSN para dirigir la activación a un equipo cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="08e65-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="08e65-111">Para obtener más información acerca de los nombres de cola, consulte la tabla de parámetros en la sección "parámetros de moniker de cola" de [Using the Queue moniker](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="08e65-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="08e65-112">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="08e65-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="08e65-113">Para especificar una aplicación COM+ como en cola, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="08e65-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="08e65-114">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.</span><span class="sxs-lookup"><span data-stu-id="08e65-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="08e65-115">Haga clic con el botón secundario en la aplicación para la que desea crear una cola y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="08e65-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="08e65-116">Seleccione la pestaña **puesta en cola** en el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="08e65-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="08e65-117">Active la casilla de verificación con la etiqueta **en cola: esta aplicación puede ser accesible mediante colas de MSMQ**.</span><span class="sxs-lookup"><span data-stu-id="08e65-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="08e65-118">Si la casilla de verificación **en cola** está atenuada, la aplicación no contiene ningún componente queuable.</span><span class="sxs-lookup"><span data-stu-id="08e65-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="08e65-119">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="08e65-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="08e65-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="08e65-120">Visual Basic</span></span>

<span data-ttu-id="08e65-121">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="08e65-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="08e65-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="08e65-122">C/C++</span></span>

<span data-ttu-id="08e65-123">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="08e65-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="08e65-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08e65-124">Remarks</span></span>

<span data-ttu-id="08e65-125">Las colas creadas por la biblioteca de administración de COM+ o la herramienta administrativa Servicios de componentes se marcan con el atributo transaccional de Message Queue Server.</span><span class="sxs-lookup"><span data-stu-id="08e65-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="08e65-126">Después de instalar una aplicación en cola en el servidor, se puede poner a disposición de los clientes mediante la exportación de la aplicación y la posterior importación de la aplicación en cada cliente.</span><span class="sxs-lookup"><span data-stu-id="08e65-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e65-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08e65-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e65-128">Creación de componentes de Queuable</span><span class="sxs-lookup"><span data-stu-id="08e65-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="08e65-129">Arquitectura de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="08e65-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



