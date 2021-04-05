---
title: Interfaces de guion gráfico
description: Esta sección contiene las especificaciones de referencia de las interfaces del administrador de animaciones de Windows que admiten guiones gráficos.
ms.assetid: 372D6348-3DF2-48EB-B495-BAD4E5DAAAD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fba60c480ef4c316731da6eefbe5334616a72b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077940"
---
# <a name="storyboard-interfaces"></a><span data-ttu-id="5372e-103">Interfaces de guion gráfico</span><span class="sxs-lookup"><span data-stu-id="5372e-103">Storyboard Interfaces</span></span>

<span data-ttu-id="5372e-104">Esta sección contiene las especificaciones de referencia de las interfaces del administrador de animaciones de Windows que admiten guiones gráficos.</span><span class="sxs-lookup"><span data-stu-id="5372e-104">This section contains the reference specifications for the Windows Animation Manager interfaces that support storyboards.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5372e-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5372e-105">In this section</span></span>



| <span data-ttu-id="5372e-106">Tema</span><span class="sxs-lookup"><span data-stu-id="5372e-106">Topic</span></span>                                                                                                 | <span data-ttu-id="5372e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5372e-107">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5372e-108">**IUIAnimationStoryboard**</span><span class="sxs-lookup"><span data-stu-id="5372e-108">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)<br/>                                   | <span data-ttu-id="5372e-109">Define un guion gráfico, que contiene un grupo de transiciones que se sincronizan entre sí.</span><span class="sxs-lookup"><span data-stu-id="5372e-109">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="5372e-110">**IUIAnimationStoryboard2**</span><span class="sxs-lookup"><span data-stu-id="5372e-110">**IUIAnimationStoryboard2**</span></span>](/windows/win32/api/uianimation/nn-uianimation-iuianimationstoryboard2)<br/>                                 | <span data-ttu-id="5372e-111">Define un guion gráfico, que contiene un grupo de transiciones que se sincronizan entre sí.</span><span class="sxs-lookup"><span data-stu-id="5372e-111">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="5372e-112">**IUIAnimationStoryboardEventHandler**</span><span class="sxs-lookup"><span data-stu-id="5372e-112">**IUIAnimationStoryboardEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler)<br/>           | <span data-ttu-id="5372e-113">Define métodos para controlar el estado y los eventos de actualización de un guión gráfico.</span><span class="sxs-lookup"><span data-stu-id="5372e-113">Defines methods for handling status and update events for a storyboard.</span></span><br/>                                    |
| [<span data-ttu-id="5372e-114">**IUIAnimationStoryboardEventHandler2**</span><span class="sxs-lookup"><span data-stu-id="5372e-114">**IUIAnimationStoryboardEventHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler2)<br/>         | <span data-ttu-id="5372e-115">Define métodos para controlar los eventos de guion gráfico.</span><span class="sxs-lookup"><span data-stu-id="5372e-115">Defines methods for handling storyboard events.</span></span> <br/>                                                           |
| [<span data-ttu-id="5372e-116">**IUIAnimationLoopIterationChangeHandler2**</span><span class="sxs-lookup"><span data-stu-id="5372e-116">**IUIAnimationLoopIterationChangeHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationloopiterationchangehandler2)<br/> | <span data-ttu-id="5372e-117">Define un método para controlar eventos de iteración de bucle de guiones gráficos.</span><span class="sxs-lookup"><span data-stu-id="5372e-117">Defines a method for handling storyboard loop iteration events.</span></span><br/>                                            |
| [<span data-ttu-id="5372e-118">**IUIAnimationPriorityComparison**</span><span class="sxs-lookup"><span data-stu-id="5372e-118">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)<br/>                   | <span data-ttu-id="5372e-119">Define un método para la comparación de prioridades que utiliza el administrador de animaciones para resolver conflictos de programación.</span><span class="sxs-lookup"><span data-stu-id="5372e-119">Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.</span></span><br/>  |
| [<span data-ttu-id="5372e-120">**IUIAnimationPriorityComparison2**</span><span class="sxs-lookup"><span data-stu-id="5372e-120">**IUIAnimationPriorityComparison2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison2)<br/>                 | <span data-ttu-id="5372e-121">Define un método que resuelve los conflictos de programación a través de la comparación de prioridades.</span><span class="sxs-lookup"><span data-stu-id="5372e-121">Defines a method that resolves scheduling conflicts through priority comparison.</span></span><br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="5372e-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5372e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5372e-123">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5372e-123">Interfaces</span></span>](windows-animation-reference.md)
</dt> </dl>

 

