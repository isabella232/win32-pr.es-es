---
description: Habilitar la activación JIT para un componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Habilitar la activación JIT para un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686446"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="73b13-103">Habilitar la activación JIT para un componente</span><span class="sxs-lookup"><span data-stu-id="73b13-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="73b13-104">Debe configurar un componente para que se active JIT solo cuando se escribe correctamente para admitir el servicio de activación Just-in-Time (JIT) de COM+.</span><span class="sxs-lookup"><span data-stu-id="73b13-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="73b13-105">Si un componente se desactiva entre las llamadas de método, perderá cualquier estado asociado.</span><span class="sxs-lookup"><span data-stu-id="73b13-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="73b13-106">Dado el comportamiento predeterminado de la activación JIT, no es probable que se produzca cuando no se espera, pero debe tener en cuenta los requisitos de un componente antes de cambiar su configuración y de las expectativas de los clientes que llamarán al componente.</span><span class="sxs-lookup"><span data-stu-id="73b13-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="73b13-107">Si un componente está configurado para requerir transacciones, el servicio de activación JIT de COM+ se habilita automáticamente.</span><span class="sxs-lookup"><span data-stu-id="73b13-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="73b13-108">En este caso, no se puede deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="73b13-108">You cannot disable it in this case.</span></span> <span data-ttu-id="73b13-109">Para obtener más información, consulte [configuración de transacciones](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="73b13-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="73b13-110">Cuando se habilita la activación JIT para un componente, su atributo de sincronización se establece en requerido para ese componente.</span><span class="sxs-lookup"><span data-stu-id="73b13-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="73b13-111">En este caso, no se puede cambiar la configuración de sincronización.</span><span class="sxs-lookup"><span data-stu-id="73b13-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="73b13-112">Para obtener más información, consulte [dependencias de sincronización](synchronization-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="73b13-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="73b13-113">**Para habilitar la activación JIT**</span><span class="sxs-lookup"><span data-stu-id="73b13-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="73b13-114">En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="73b13-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="73b13-115">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="73b13-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="73b13-116">Para habilitar la activación JIT para el componente, active la casilla **Habilitar activación Just-in-Time** .</span><span class="sxs-lookup"><span data-stu-id="73b13-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="73b13-117">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="73b13-117">Click **OK**.</span></span>

<span data-ttu-id="73b13-118">Cuando haya habilitado la activación JIT para un componente, tiene la opción de habilitar la característica de Autocompletar para cualquier método expuesto por ese componente.</span><span class="sxs-lookup"><span data-stu-id="73b13-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="73b13-119">Consulte [habilitación de la función automática para un método](enabling-auto-done-for-a-method.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="73b13-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73b13-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73b13-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73b13-121">Habilitar auto-Done para un método</span><span class="sxs-lookup"><span data-stu-id="73b13-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="73b13-122">Establecer el bit Done</span><span class="sxs-lookup"><span data-stu-id="73b13-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



