---
title: Controles (COM)
description: Controles
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359597"
---
# <a name="controls-com"></a><span data-ttu-id="aed29-103">Controles (COM)</span><span class="sxs-lookup"><span data-stu-id="aed29-103">Controls (COM)</span></span>

<span data-ttu-id="aed29-104">Un control ActiveX es realmente simplemente otro término para el objeto OLE o más específicamente, un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="aed29-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="aed29-105">En otras palabras, un control, como mínimo, es un objeto COM que admite la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y también se registra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="aed29-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="aed29-106">A través de [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , un contenedor puede administrar la duración del control y detectar dinámicamente el alcance completo de la funcionalidad de un control basándose en las interfaces disponibles.</span><span class="sxs-lookup"><span data-stu-id="aed29-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="aed29-107">Esto permite a un control implementar la menor funcionalidad que necesita, en lugar de admitir un gran número de interfaces que realmente no hacen nada.</span><span class="sxs-lookup"><span data-stu-id="aed29-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="aed29-108">En Resumen, este requisito mínimo para nada más que **IUnknown** permite que cualquier control sea tan ligero como pueda.</span><span class="sxs-lookup"><span data-stu-id="aed29-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="aed29-109">En Resumen, aparte de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y el registro automático, no hay ningún otro requisito para un control.</span><span class="sxs-lookup"><span data-stu-id="aed29-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="aed29-110">Sin embargo, hay convenciones que se deben seguir sobre lo que significa la compatibilidad de una interfaz en cuanto a la funcionalidad proporcionada por el control por parte del contenedor.</span><span class="sxs-lookup"><span data-stu-id="aed29-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="aed29-111">En esta sección se describe lo que significa que un control admite realmente una interfaz, así como métodos, propiedades y eventos que un control debe proporcionar como línea base si tiene ocasión de admitir métodos, propiedades y eventos.</span><span class="sxs-lookup"><span data-stu-id="aed29-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="aed29-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="aed29-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="aed29-113">Registro propio para controles</span><span class="sxs-lookup"><span data-stu-id="aed29-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="aed29-114">Compatibilidad con una interfaz</span><span class="sxs-lookup"><span data-stu-id="aed29-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="aed29-115">Interfaces de persistencia</span><span class="sxs-lookup"><span data-stu-id="aed29-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="aed29-116">Métodos opcionales en interfaces de control</span><span class="sxs-lookup"><span data-stu-id="aed29-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="aed29-117">Opciones del generador de clases</span><span class="sxs-lookup"><span data-stu-id="aed29-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="aed29-118">Exponer propiedades a través de IDispatch</span><span class="sxs-lookup"><span data-stu-id="aed29-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="aed29-119">Exponer métodos a través de IDispatch</span><span class="sxs-lookup"><span data-stu-id="aed29-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="aed29-120">Eventos en controles</span><span class="sxs-lookup"><span data-stu-id="aed29-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="aed29-121">Páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="aed29-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="aed29-122">Propiedades de ambiente para controles</span><span class="sxs-lookup"><span data-stu-id="aed29-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="aed29-123">Usar la funcionalidad del contenedor</span><span class="sxs-lookup"><span data-stu-id="aed29-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="aed29-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aed29-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aed29-125">Directrices para el contenedor de controles y controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="aed29-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




