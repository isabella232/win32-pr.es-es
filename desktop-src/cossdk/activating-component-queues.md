---
description: Activación de colas de componentes
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Activación de colas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423320"
---
# <a name="activating-component-queues"></a><span data-ttu-id="5478b-103">Activación de colas de componentes</span><span class="sxs-lookup"><span data-stu-id="5478b-103">Activating Component Queues</span></span>

<span data-ttu-id="5478b-104">La realización de llamadas a métodos en un componente en cola no ejecuta directamente el método.</span><span class="sxs-lookup"><span data-stu-id="5478b-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="5478b-105">En su lugar, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) calcula las referencias y almacena llamadas y parámetros de métodos en una cola en la que más adelante se recuperan y ejecutan mediante el componente en cola.</span><span class="sxs-lookup"><span data-stu-id="5478b-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="5478b-106">A diferencia de la activación de un objeto DCOM remoto, no se crea una instancia del componente en cola cuando se llama a un método.</span><span class="sxs-lookup"><span data-stu-id="5478b-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="5478b-107">Esta es la idea básica detrás del uso de componentes en cola; no es necesario crear instancias de los componentes en cola al mismo tiempo que la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="5478b-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="5478b-108">En las descripciones para activar una aplicación en cola se supone que la aplicación está marcada como en cola y que la casilla del agente de escucha está habilitada.</span><span class="sxs-lookup"><span data-stu-id="5478b-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="5478b-109">Puede usar scripts para iniciar y detener una aplicación en cola.</span><span class="sxs-lookup"><span data-stu-id="5478b-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="5478b-110">Puede colocar el script bajo el control del programador de tareas para ejecutarlo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5478b-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="5478b-111">Por ejemplo, el script se puede ejecutar en el reinicio del sistema si las aplicaciones están disponibles de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="5478b-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="5478b-112">Si la aplicación va a procesar transacciones en modo por lotes, el script se puede ejecutar en un momento determinado cada día junto con un script de cierre para asegurarse de que el procesamiento por lotes se detiene en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="5478b-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="5478b-113">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="5478b-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="5478b-114">Para iniciar una aplicación en cola, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="5478b-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="5478b-115">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.</span><span class="sxs-lookup"><span data-stu-id="5478b-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="5478b-116">Haga clic con el botón secundario en la aplicación cuya cola desee activar.</span><span class="sxs-lookup"><span data-stu-id="5478b-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="5478b-117">Haga clic en **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="5478b-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="5478b-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5478b-118">Visual Basic</span></span>

<span data-ttu-id="5478b-119">Vea el ejemplo de COMAdminCatalog. StartApplication.</span><span class="sxs-lookup"><span data-stu-id="5478b-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="5478b-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="5478b-120">C/C++</span></span>

<span data-ttu-id="5478b-121">Vea el ejemplo [**ICOMAdminCatalog:: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .</span><span class="sxs-lookup"><span data-stu-id="5478b-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5478b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5478b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5478b-123">Usar el moniker de cola</span><span class="sxs-lookup"><span data-stu-id="5478b-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



