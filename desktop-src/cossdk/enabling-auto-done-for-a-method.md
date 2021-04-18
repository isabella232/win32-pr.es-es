---
description: Puede habilitar la característica auto-Done para cualquier método expuesto por un componente para el que esté habilitada la activación JIT de COM+. Si la activación JIT está deshabilitada, la operación automática no está disponible.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Habilitar auto-Done para un método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714871"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="bdf32-104">Habilitar auto-Done para un método</span><span class="sxs-lookup"><span data-stu-id="bdf32-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="bdf32-105">Puede habilitar la característica auto-Done para cualquier método expuesto por un componente para el que esté habilitada la activación JIT de COM+.</span><span class="sxs-lookup"><span data-stu-id="bdf32-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="bdf32-106">Si la activación JIT está deshabilitada, la operación automática no está disponible.</span><span class="sxs-lookup"><span data-stu-id="bdf32-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="bdf32-107">Debe habilitar la función auto-Done solo para un método que se ha escrito intencionadamente para aprovecharlo porque esta característica puede cambiar el comportamiento esperado del método.</span><span class="sxs-lookup"><span data-stu-id="bdf32-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="bdf32-108">Cuando habilita auto-Done, cambia el comportamiento predeterminado de la activación JIT y las transacciones automáticas para ese método.</span><span class="sxs-lookup"><span data-stu-id="bdf32-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="bdf32-109">Puede que desee usar esta característica porque puede quitar la necesidad de declarar explícitamente la coherencia y la realización.</span><span class="sxs-lookup"><span data-stu-id="bdf32-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="bdf32-110">En su lugar, esto se puede hacer simplemente devolviendo un valor HRESULT cuando está habilitada la operación automática.</span><span class="sxs-lookup"><span data-stu-id="bdf32-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="bdf32-111">En esencia, cuando se habilita auto-Done, se indica a COM+ que haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bdf32-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="bdf32-112">Establezca el bit done en true de forma predeterminada en el contexto en el que se ejecuta el objeto cada vez que se llama a este método.</span><span class="sxs-lookup"><span data-stu-id="bdf32-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="bdf32-113">Inspeccione el HRESULT devuelto por el método; Si indica éxito o error, establezca el bit de coherencia en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="bdf32-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="bdf32-114">Esto puede dar lugar a una llamada automática a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), dependiendo también de lo que el método hace internamente.</span><span class="sxs-lookup"><span data-stu-id="bdf32-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="bdf32-115">**Para habilitar la función automática para un método**</span><span class="sxs-lookup"><span data-stu-id="bdf32-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="bdf32-116">En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el método que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="bdf32-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="bdf32-117">En el cuadro de diálogo Propiedades del método, haga clic en la pestaña **General** .</span><span class="sxs-lookup"><span data-stu-id="bdf32-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="bdf32-118">Para habilitar la función automática, active la casilla **desactivar automáticamente este objeto cuando se devuelva este método** .</span><span class="sxs-lookup"><span data-stu-id="bdf32-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="bdf32-119">Si la casilla no está disponible, primero debe habilitar la activación JIT para el componente.</span><span class="sxs-lookup"><span data-stu-id="bdf32-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="bdf32-120">(Consulte[habilitación de la activación JIT para un componente](enabling-jit-activation-for-a-component.md) para obtener instrucciones detalladas).</span><span class="sxs-lookup"><span data-stu-id="bdf32-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="bdf32-121">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdf32-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdf32-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdf32-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdf32-123">Conceptos de activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="bdf32-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="bdf32-124">Habilitar la activación JIT para un componente</span><span class="sxs-lookup"><span data-stu-id="bdf32-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="bdf32-125">Establecer el bit Done</span><span class="sxs-lookup"><span data-stu-id="bdf32-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



