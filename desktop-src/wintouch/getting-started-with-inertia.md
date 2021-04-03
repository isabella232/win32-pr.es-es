---
title: Inercia
description: En esta sección se explica la inercia de Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch, inercia
- inercia, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075207"
---
# <a name="inertia"></a><span data-ttu-id="151d1-105">Inercia</span><span class="sxs-lookup"><span data-stu-id="151d1-105">Inertia</span></span>

<span data-ttu-id="151d1-106">En esta sección se explica la inercia de Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="151d1-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="151d1-107">La API de inercia incluida en Windows 7 permite el comportamiento de objetos coherentes en las aplicaciones táctiles de Windows al proporcionar un modelo físico simple.</span><span class="sxs-lookup"><span data-stu-id="151d1-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="151d1-108">La inercia se habilita mediante el procesador de inercia, una clase que encapsula la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="151d1-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="151d1-109">El procesador de inercia funciona mediante el procesamiento de eventos que se le pasan cuando las manipulaciones de objetos finalizan y controlan las trayectorias de objeto de una manera coherente con otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="151d1-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="151d1-110">Tenga en cuenta que el procesador de inercia está estrechamente acoplado al procesador de manipulación para simplificar la adición de compatibilidad de inercia a las aplicaciones que usan manipulaciones.</span><span class="sxs-lookup"><span data-stu-id="151d1-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="151d1-111">De hecho, el procesador de inercia genera los mismos eventos que el procesador de manipulación.</span><span class="sxs-lookup"><span data-stu-id="151d1-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="151d1-112">En la siguiente sección se explica cómo empezar a usar la inercia.</span><span class="sxs-lookup"><span data-stu-id="151d1-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="151d1-113">Sección</span><span class="sxs-lookup"><span data-stu-id="151d1-113">Section</span></span>                                                                      | <span data-ttu-id="151d1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="151d1-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="151d1-115">Mecánica de inercia</span><span class="sxs-lookup"><span data-stu-id="151d1-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="151d1-116">Explica los conceptos básicos de los cálculos de inercia.</span><span class="sxs-lookup"><span data-stu-id="151d1-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="151d1-117">Controlar la inercia en código no administrado</span><span class="sxs-lookup"><span data-stu-id="151d1-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="151d1-118">Explica cómo usar la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para controlar la inercia en el código no administrado.</span><span class="sxs-lookup"><span data-stu-id="151d1-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="151d1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="151d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="151d1-120">Manipulaciones e inercia</span><span class="sxs-lookup"><span data-stu-id="151d1-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




