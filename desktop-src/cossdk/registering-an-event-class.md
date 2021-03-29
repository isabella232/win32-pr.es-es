---
description: Para que los suscriptores puedan encontrar una clase de eventos y suscribirse a ella, las clases de eventos deben estar registradas en el catálogo de COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrar una clase de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807369"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="122e1-103">Registrar una clase de eventos</span><span class="sxs-lookup"><span data-stu-id="122e1-103">Registering an Event Class</span></span>

<span data-ttu-id="122e1-104">Para que los suscriptores puedan encontrar una clase de eventos y suscribirse a ella, las clases de eventos deben estar registradas en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="122e1-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="122e1-105">COM+ requiere una biblioteca de tipos que describa los métodos y las interfaces de eventos para que pueda coincidir y conectar correctamente los suscriptores y los publicadores.</span><span class="sxs-lookup"><span data-stu-id="122e1-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="122e1-106">La biblioteca de tipos debe residir o ir acompañada de un archivo DLL de registro automático.</span><span class="sxs-lookup"><span data-stu-id="122e1-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="122e1-107">Puede usar la herramienta administrativa Servicios de componentes o las funciones administrativas de COM+ para registrar una clase de eventos en el catálogo de COM+.</span><span class="sxs-lookup"><span data-stu-id="122e1-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="122e1-108">**Para registrar una clase de eventos con la herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="122e1-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="122e1-109">Crear una nueva aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="122e1-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="122e1-110">Abra la carpeta de la aplicación y seleccione **componentes**.</span><span class="sxs-lookup"><span data-stu-id="122e1-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="122e1-111">En el menú **Acción**, haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="122e1-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="122e1-112">(También puede seleccionar la carpeta **componentes** , hacer clic con el botón secundario, elegir **nuevo** y hacer clic en **componente**).</span><span class="sxs-lookup"><span data-stu-id="122e1-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="122e1-113">Haga clic en **instalar nuevas clases de eventos**.</span><span class="sxs-lookup"><span data-stu-id="122e1-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="122e1-114">Escriba la ruta de acceso al archivo DLL del componente de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="122e1-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="122e1-115">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="122e1-115">Click **OK**.</span></span>

<span data-ttu-id="122e1-116">La clase de eventos se registra en el catálogo de COM+ y la pueden encontrar los suscriptores interesados en obtener la información proporcionada por la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="122e1-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="122e1-117">Para obtener información sobre cómo registrar la clase de eventos mediante las interfaces administrativas de COM+, vea [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span><span class="sxs-lookup"><span data-stu-id="122e1-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="122e1-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="122e1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="122e1-119">Registro de una suscripción</span><span class="sxs-lookup"><span data-stu-id="122e1-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



