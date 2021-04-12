---
description: En esta información general se presentan varios métodos de XAudio2 que se pueden llamar como parte de un conjunto de operaciones.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Conjuntos de operaciones de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279359"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="c9d3a-103">Conjuntos de operaciones de XAudio2</span><span class="sxs-lookup"><span data-stu-id="c9d3a-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="c9d3a-104">En esta información general se presentan varios métodos de XAudio2 que se pueden llamar como parte de un conjunto de operaciones.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="c9d3a-105">Varios métodos de XAudio2 toman el argumento *OperationSet* , que permite que se llamen como parte de un grupo diferido.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="c9d3a-106">En un momento dado, puede aplicar un conjunto completo de cambios simultáneamente llamando a la función [**IXAudio2:: commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el identificador *OperationSet* para ese grupo.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="c9d3a-107">El identificador es un número arbitrario.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="c9d3a-108">Por lo tanto, permite que partes independientes del código de cliente apliquen cambios atómicos independientes al gráfico sin ningún conflicto.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="c9d3a-109">La práctica recomendada es que el cliente incremente un contador global siempre que necesite generar un identificador único de *OperationSet* .</span><span class="sxs-lookup"><span data-stu-id="c9d3a-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="c9d3a-110">Se garantiza que un conjunto de cambios en el gráfico, aplicados de forma atómica, es preciso para la muestra.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="c9d3a-111">Por ejemplo, las voces se iniciarán en sincronización.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="c9d3a-112">Si establece *OperationSet* en \_ la confirmación de XAUDIO2 \_ Now, el cambio se aplica inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="c9d3a-113">Surte efecto en el primer paso de procesamiento de audio después de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="c9d3a-114">Si llama a [**commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con \_ la confirmación de XAUDIO2 \_ All, se realizan cambios en todos los conjuntos de operaciones pendientes, independientemente de su identificador *OperationSet* .</span><span class="sxs-lookup"><span data-stu-id="c9d3a-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="c9d3a-115">Ciertos métodos surten efecto inmediatamente cuando se les llama desde una devolución de llamada de XAudio2 con un *OperationSet* de la confirmación de xaudio2 \_ \_ ahora.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="c9d3a-116">Todos los demás métodos que toman un argumento *OperationSet* solo surten efecto en el siguiente paso de procesamiento una vez que se llama al método (si se llama con la confirmación de XAUDIO2 \_ \_ ahora), o después de llamar a [**commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el mismo *OperationSet*.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="c9d3a-117">Debido a esto, es posible que ciertas llamadas al método no se realicen siempre en el mismo orden en el que se llamaron.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="c9d3a-118">Todas las operaciones pendientes se confirman de forma atómica cuando se llama a [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) .</span><span class="sxs-lookup"><span data-stu-id="c9d3a-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="c9d3a-119">Los métodos a los que se llama mientras se detiene el motor surten efecto inmediatamente, independientemente del valor de *OperationSet* proporcionado.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="c9d3a-120">Al reiniciar el motor, XAudio2 vuelve al modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="c9d3a-121">Los escenarios simples en los que los conjuntos de operaciones son útiles son los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="c9d3a-122">Iniciar varias voces simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="c9d3a-123">Enviar simultáneamente un búfer a una voz, establecer los parámetros de voz e iniciar la voz.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="c9d3a-124">Realización de un cambio a gran escala en el gráfico, como la conexión de todas las voces de origen a una nueva voz de submezcla.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="c9d3a-125">Vea [Cómo: agrupar métodos de audio como un conjunto de operaciones](how-to--group-audio-methods-as-an-operation-set.md) para obtener un ejemplo del uso de un conjunto de operaciones.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="c9d3a-126">Métodos de conjunto de operaciones</span><span class="sxs-lookup"><span data-stu-id="c9d3a-126">Operation Set Methods</span></span>

<span data-ttu-id="c9d3a-127">Puede llamar a los métodos siguientes como parte de un conjunto de operaciones.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="c9d3a-128">**IXAudio2SourceVoice::ExitLoop**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="c9d3a-129">**IXAudio2Voice::SetFilterParameters**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="c9d3a-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="c9d3a-131">**IXAudio2Voice::D isableEffect**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="c9d3a-132">**IXAudio2Voice::EnableEffect**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="c9d3a-133">**IXAudio2Voice::SetChannelVolumes**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="c9d3a-134">**IXAudio2Voice::SetEffectParameters**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="c9d3a-135">**IXAudio2Voice::SetOutputMatrix**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="c9d3a-136">**IXAudio2Voice::SetVolume**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="c9d3a-137">**IXAudio2SourceVoice:: Start**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="c9d3a-138">**IXAudio2SourceVoice:: Stop**</span><span class="sxs-lookup"><span data-stu-id="c9d3a-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="c9d3a-139">Tal y como se ha descrito anteriormente, el código de cliente debe llamar finalmente a la función [**IXAudio2:: commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) para ejecutar los cambios aplazados.</span><span class="sxs-lookup"><span data-stu-id="c9d3a-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9d3a-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d3a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d3a-141">Conjuntos de operaciones</span><span class="sxs-lookup"><span data-stu-id="c9d3a-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="c9d3a-142">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="c9d3a-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="c9d3a-143">Cómo: agrupar métodos de audio como un conjunto de operaciones</span><span class="sxs-lookup"><span data-stu-id="c9d3a-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
