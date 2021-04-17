---
description: Un componente COM configurado normalmente se activa en su propio contexto; es decir, COM+ hace referencia a la información del catálogo de componentes para proporcionar los servicios configurados.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Forzar la activación en el contexto predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539424"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="6ba03-103">Forzar la activación en el contexto predeterminado</span><span class="sxs-lookup"><span data-stu-id="6ba03-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="6ba03-104">Un componente COM configurado normalmente se activa en su propio contexto; es decir, COM+ hace referencia a la información de catálogo del componente para proporcionar los servicios configurados.</span><span class="sxs-lookup"><span data-stu-id="6ba03-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="6ba03-105">Sin embargo, puede optar por activar un componente configurado en el contexto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ba03-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="6ba03-106">Un componente COM base (un componente registrado que no tiene información de catálogo de COM+) se activa normalmente en el contexto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ba03-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="6ba03-107">La activación de un componente COM en el contexto predeterminado proporciona tres ventajas de rendimiento principales, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6ba03-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="6ba03-108">Los recursos del sistema se guardan limitando el número de contextos que se crean.</span><span class="sxs-lookup"><span data-stu-id="6ba03-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="6ba03-109">Para aumentar el rendimiento, limite el número de llamadas entre contextos.</span><span class="sxs-lookup"><span data-stu-id="6ba03-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="6ba03-110">Dado que las llamadas entre contextos requieren serialización, es mucho más rápido que un objeto COM activado en el contexto predeterminado realice llamadas a otros objetos en el contexto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ba03-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="6ba03-111">El rendimiento en este caso (de llamadas dentro del mismo contexto) es similar al de llamar a una subrutina.</span><span class="sxs-lookup"><span data-stu-id="6ba03-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="6ba03-112">Puede importar aplicaciones COM antiguas en COM+ y ejecutarlas sin problemas.</span><span class="sxs-lookup"><span data-stu-id="6ba03-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="6ba03-113">Por ejemplo, puede tener varias aplicaciones COM anteriores implementadas bajo la suposición de que se permite pasar referencias de objeto dentro de un apartamento sin calcular las referencias de las referencias.</span><span class="sxs-lookup"><span data-stu-id="6ba03-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="6ba03-114">Estas aplicaciones COM no funcionan cuando se importan en COM+ porque las referencias de objeto se pasan a través de los límites del contexto.</span><span class="sxs-lookup"><span data-stu-id="6ba03-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="6ba03-115">Sin embargo, puede hacer que este tipo de aplicación COM se ejecute cuando se importe si usa la herramienta administrativa Servicios de componentes para marcar todas las clases de la aplicación como **se debe activar en el contexto predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="6ba03-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="6ba03-116">La principal desventaja de activar un componente configurado en el contexto predeterminado es que COM+ no proporciona ninguno de los servicios configurados del componente.</span><span class="sxs-lookup"><span data-stu-id="6ba03-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="6ba03-117">Hay un equilibrio entre el rendimiento mejorado y la capacidad de usar los servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="6ba03-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="6ba03-118">Por ejemplo, supongamos que un componente COM no requiere ningún servicio COM+ (como [transacciones](com--transactions.md), [activación Just-in-Time](com--just-in-time-activation.md), [eventos](com--events.md), [componentes en cola](com--queued-components.md), [sincronización](com--synchronization.md)o [agrupación de objetos](com--object-pooling.md)) y que el componente realiza varias llamadas a otros componentes com que se pueden activar en el contexto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ba03-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="6ba03-119">En este caso, sería una buena idea activar el componente de llamada en el contexto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6ba03-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="6ba03-120">Si el componente COM requiere servicios COM+, no se puede marcar como **se debe activar en el contexto predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="6ba03-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="6ba03-121">Además, no hay ninguna ganancia de rendimiento real si un objeto COM activado en el contexto predeterminado realiza varias llamadas a objetos en otros contextos.</span><span class="sxs-lookup"><span data-stu-id="6ba03-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="6ba03-122">(Para obtener más información, vea [contextos](com--contexts.md)).</span><span class="sxs-lookup"><span data-stu-id="6ba03-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="6ba03-123">**Para aplicar la activación en el contexto predeterminado**</span><span class="sxs-lookup"><span data-stu-id="6ba03-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="6ba03-124">En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente (ubicado en la carpeta **componentes** de cualquier aplicación com+ seleccionada) que desee activar en el contexto predeterminado y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6ba03-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="6ba03-125">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="6ba03-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="6ba03-126">Active la casilla **debe activarse en el contexto predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="6ba03-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="6ba03-127">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ba03-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="6ba03-128">Al ejecutar un componente configurado en el contexto predeterminado, COM+ no activa ninguno de los servicios configurados para ese componente.</span><span class="sxs-lookup"><span data-stu-id="6ba03-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="6ba03-129">Estos servicios están disponibles de nuevo cuando se desactiva la casilla **se debe activar en el contexto predeterminado** y, posteriormente, se ejecuta el componente configurado en su propio contexto.</span><span class="sxs-lookup"><span data-stu-id="6ba03-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6ba03-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ba03-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ba03-131">Conceptos de activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="6ba03-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="6ba03-132">Forzar la activación en el contexto del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="6ba03-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



