---
title: Agregar una referencia a un proyecto de Visual Basic
description: Agregar una referencia a un proyecto de Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356949"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="3aef1-103">Agregar una referencia a un proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3aef1-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="3aef1-104">En el procedimiento siguiente se describe cómo agregar una referencia a un objeto COM en un proyecto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3aef1-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="3aef1-105">A continuación, la aplicación puede usar las clases de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="3aef1-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="3aef1-106">Cuando se agrega un objeto como referencia, solo se puede utilizar la biblioteca de tipos proporcionada por el control o la biblioteca de tipos "sin procesar".</span><span class="sxs-lookup"><span data-stu-id="3aef1-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="3aef1-107">En cambio, al agregar un control como componente también se exponen las propiedades y los métodos del extensor Visual Basic como si formaran parte del control.</span><span class="sxs-lookup"><span data-stu-id="3aef1-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="3aef1-108">**Para hacer referencia Visual Basic a un componente**</span><span class="sxs-lookup"><span data-stu-id="3aef1-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="3aef1-109">En el menú **Proyecto**, haga clic en **Referencias**.</span><span class="sxs-lookup"><span data-stu-id="3aef1-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="3aef1-110">Active la casilla situada junto al componente que desee agregar.</span><span class="sxs-lookup"><span data-stu-id="3aef1-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="3aef1-111">Si el componente no aparece en la lista, busque el archivo. dll o. ocx mediante **examinar**.</span><span class="sxs-lookup"><span data-stu-id="3aef1-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="3aef1-112">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="3aef1-112">Click **OK**.</span></span>

<span data-ttu-id="3aef1-113">El componente ahora forma parte del proyecto.</span><span class="sxs-lookup"><span data-stu-id="3aef1-113">The component is now part of the project.</span></span> <span data-ttu-id="3aef1-114">La aplicación puede crear instancias de clase mediante la palabra clave **New** .</span><span class="sxs-lookup"><span data-stu-id="3aef1-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aef1-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3aef1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aef1-116">Agregar un componente a un proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3aef1-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="3aef1-117">Trasladar a Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3aef1-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




