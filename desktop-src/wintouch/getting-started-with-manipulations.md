---
title: Manipulaciones
description: En esta sección se explica la manipulación de objetos para Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch, manipulaciones
- manipulaciones, acerca de
- manipulaciones, diferencias de gestos
- gestos, diferencias de manipulación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356757"
---
# <a name="manipulations"></a><span data-ttu-id="6d3bb-107">Manipulaciones</span><span class="sxs-lookup"><span data-stu-id="6d3bb-107">Manipulations</span></span>

<span data-ttu-id="6d3bb-108">En esta sección se explica la manipulación de objetos para Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="6d3bb-109">Información general sobre la manipulación</span><span class="sxs-lookup"><span data-stu-id="6d3bb-109">Manipulation Overview</span></span>

<span data-ttu-id="6d3bb-110">Una manera cómoda de pensar en las manipulaciones es considerarlas un superconjunto de gestos.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="6d3bb-111">Lo que puede hacer con los gestos, puede hacerlo con más flexibilidad y con una precisión más precisa mediante el uso de manipulaciones.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="6d3bb-112">La diferencia entre las manipulaciones y los gestos se demuestra mejor con un ejemplo sencillo.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="6d3bb-113">Puede expandir un objeto y, al mismo tiempo, convertirlo mediante manipulaciones; con los gestos, solo puede realizar una vez.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="6d3bb-114">Esta capacidad de manipular un objeto en tiempo real hace que las aplicaciones sean más intuitivas para los usuarios al habilitar una experiencia más realista.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="6d3bb-115">Las API de manipulación se utilizan para simplificar las operaciones de transformación en objetos para aplicaciones habilitadas para toque.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="6d3bb-116">Las manipulaciones se realizan en Windows 7 a través del objeto COM Manipulations.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="6d3bb-117">Mediante el uso de manipulaciones, los desarrolladores pueden admitir con mayor facilidad la inercia (física de objetos) y pueden realizar transformaciones con facilidad en objetos de una manera coherente con otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="6d3bb-118">En las secciones siguientes se explican varias maneras en las que puede realizar manipulaciones.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="6d3bb-119">Sección</span><span class="sxs-lookup"><span data-stu-id="6d3bb-119">Section</span></span>                                                                                            | <span data-ttu-id="6d3bb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d3bb-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d3bb-121">Agregar compatibilidad de manipulación a código no administrado</span><span class="sxs-lookup"><span data-stu-id="6d3bb-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="6d3bb-122">Explica cómo implementar un receptor de eventos para la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) y agregar controladores de eventos al código.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="6d3bb-123">Manipulaciones avanzadas</span><span class="sxs-lookup"><span data-stu-id="6d3bb-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="6d3bb-124">Explica cómo realizar manipulaciones complejas.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="6d3bb-125">Rotación de un solo dedo</span><span class="sxs-lookup"><span data-stu-id="6d3bb-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="6d3bb-126">Explica cómo girar un objeto utilizando un punto de pivote y el procesador de manipulación.</span><span class="sxs-lookup"><span data-stu-id="6d3bb-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="6d3bb-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d3bb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d3bb-128">Manipulaciones e inercia</span><span class="sxs-lookup"><span data-stu-id="6d3bb-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




