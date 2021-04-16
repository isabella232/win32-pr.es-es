---
description: Forzar la activación en el contexto de llamadores
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Forzar la activación en el contexto de llamadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686432"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="61044-103">Forzar la activación en el contexto del autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="61044-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="61044-104">Puede controlar si un objeto se activa en su propio contexto.</span><span class="sxs-lookup"><span data-stu-id="61044-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="61044-105">Cuando se usa la herramienta administrativa Servicios de componentes para requerir la activación del componente en el contexto del autor de la llamada, ocurre lo siguiente cuando COM+ activa una instancia del componente en un contexto:</span><span class="sxs-lookup"><span data-stu-id="61044-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="61044-106">Si es posible, el objeto se activa en el contexto del creador.</span><span class="sxs-lookup"><span data-stu-id="61044-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="61044-107">Se produce un error en la activación del objeto si necesita su propio contexto; \_ \_ \_ Se devuelve el intento de \_ crear un contexto de \_ \_ cliente externo \_ .</span><span class="sxs-lookup"><span data-stu-id="61044-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="61044-108">El hecho de que el objeto requiera o no su propio contexto depende de su configuración en relación con el estado actual de las propiedades de contexto del llamador.</span><span class="sxs-lookup"><span data-stu-id="61044-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="61044-109">Para obtener más información, vea [contextos de com+](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="61044-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="61044-110">Querrá controlar la activación en ese nivel de precisión si algún aspecto del objeto no funcionaría correctamente si tiene su propio contexto.</span><span class="sxs-lookup"><span data-stu-id="61044-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="61044-111">Por ejemplo, si el componente no admite el cálculo de referencias y tiene su propio contexto, se producirá un error en cualquier llamada a él porque se interceptan las llamadas entre contextos y se realiza una serialización ligera.</span><span class="sxs-lookup"><span data-stu-id="61044-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="61044-112">**Para aplicar la activación en el contexto del autor de la llamada**</span><span class="sxs-lookup"><span data-stu-id="61044-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="61044-113">En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente (ubicado en la carpeta **componentes** de cualquier aplicación com+ seleccionada) para el que está configurando las propiedades de activación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="61044-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="61044-114">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="61044-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="61044-115">Active la casilla **debe activarse en el contexto de llamadores** .</span><span class="sxs-lookup"><span data-stu-id="61044-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="61044-116">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="61044-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61044-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61044-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61044-118">Conceptos de activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="61044-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="61044-119">Forzar la activación en el contexto predeterminado</span><span class="sxs-lookup"><span data-stu-id="61044-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



