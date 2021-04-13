---
description: Cuando un objeto se activa en un contexto determinado, las llamadas subsiguientes a o desde él, dentro del contexto, se tratan de manera diferente que las llamadas en el límite del contexto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interceptación de llamadas entre contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360051"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="571a0-103">Interceptación de llamadas entre contextos</span><span class="sxs-lookup"><span data-stu-id="571a0-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="571a0-104">Cuando un objeto se activa en un contexto determinado, las llamadas subsiguientes a o desde él, dentro del contexto, se tratan de manera diferente que las llamadas en el límite del contexto.</span><span class="sxs-lookup"><span data-stu-id="571a0-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="571a0-105">Las llamadas en el límite del contexto se administran con servidores proxy ligeros.</span><span class="sxs-lookup"><span data-stu-id="571a0-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="571a0-106">Estos proxies controlan cualquier mediación necesaria para ajustar el entorno en tiempo de ejecución desde uno que admita al llamador a uno que se acomode al destinatario.</span><span class="sxs-lookup"><span data-stu-id="571a0-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="571a0-107">Este proceso se conoce como *intercepción*.</span><span class="sxs-lookup"><span data-stu-id="571a0-107">This process is known as *interception*.</span></span>

<span data-ttu-id="571a0-108">La intercepción de llamadas entre contextos es necesaria porque los objetos de contextos diferentes tienen requisitos de tiempo de ejecución diferentes, es precisamente el motivo de los contextos.</span><span class="sxs-lookup"><span data-stu-id="571a0-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="571a0-109">COM+ intercepta las referencias a objetos que se pasan como parámetros de método y las convierte automáticamente en servidores proxy para que se puedan usar en el nuevo contexto.</span><span class="sxs-lookup"><span data-stu-id="571a0-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="571a0-110">Si comparte referencias a objetos entre los límites del contexto por otros medios (por ejemplo, en variables globales) siempre debe usar [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) y [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="571a0-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="571a0-111">Estas funciones pueden traducir una referencia de objeto en un proxy que se puede usar en un contexto diferente.</span><span class="sxs-lookup"><span data-stu-id="571a0-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="571a0-112">Nunca comparta una referencia de objeto sin formato a través de los límites del contexto.</span><span class="sxs-lookup"><span data-stu-id="571a0-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="571a0-113">El comportamiento de las llamadas en el contexto puede tener consecuencias no deseadas en el caso de los objetos que exponen interfaces en las que no se pueden calcular las referencias.</span><span class="sxs-lookup"><span data-stu-id="571a0-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="571a0-114">En este caso, es probable que desee insistir en que el objeto al que no se pueden calcular las referencias se active solo en el contexto de su llamador y nunca en su propio contexto.</span><span class="sxs-lookup"><span data-stu-id="571a0-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="571a0-115">Para ello, seleccione la opción **debe activarse en el contexto del autor** de la llamada en la pestaña **activación** de la página **propiedades** del componente.</span><span class="sxs-lookup"><span data-stu-id="571a0-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="571a0-116">(Vea [forzar la activación en el contexto del autor de la llamada](enforcing-activation-in-the-caller-s-context.md) para obtener instrucciones paso a paso).</span><span class="sxs-lookup"><span data-stu-id="571a0-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="571a0-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="571a0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="571a0-118">Activación de contexto</span><span class="sxs-lookup"><span data-stu-id="571a0-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
