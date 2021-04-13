---
title: Agregar un componente a un proyecto de Visual Basic
description: Agregar un componente a un proyecto de Visual Basic
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356950"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a><span data-ttu-id="8c5b9-103">Agregar un componente a un proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8c5b9-103">Adding a Component to a Visual Basic Project</span></span>

<span data-ttu-id="8c5b9-104">En el procedimiento siguiente se describe cómo agregar un objeto COM como componente a un proyecto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-104">The following procedure describes how to add a COM object as a component to a Visual Basic project.</span></span> <span data-ttu-id="8c5b9-105">A continuación, la aplicación puede usar las clases de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="8c5b9-106">Al agregar un control como componente, se exponen las propiedades y los métodos del extensor Visual Basic como si formaran parte del control.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-106">Adding a control as a component exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span> <span data-ttu-id="8c5b9-107">Por el contrario, cuando se agrega un objeto como referencia, solo se puede usar la biblioteca de tipos proporcionada por el control o la biblioteca de tipos "sin procesar".</span><span class="sxs-lookup"><span data-stu-id="8c5b9-107">In contrast, when you add an object as a reference you can only use the type library provided by the control, or the "raw" type library.</span></span>

<span data-ttu-id="8c5b9-108">**Para insertar un control en un proyecto de Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="8c5b9-108">**To insert a control into a Visual Basic project**</span></span>

1.  <span data-ttu-id="8c5b9-109">En el menú **Proyecto**, haga clic en **Componentes**.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-109">On the **Project** menu, click **Components**.</span></span>
2.  <span data-ttu-id="8c5b9-110">Active la casilla situada junto al componente que desee agregar.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="8c5b9-111">Si el componente no aparece en la lista, busque el archivo. dll o. ocx mediante **examinar**.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="8c5b9-112">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-112">Click **OK**.</span></span>

<span data-ttu-id="8c5b9-113">El componente ahora forma parte del proyecto y aparece en la barra de herramientas de objeto.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-113">The component is now part of the project and appears in the object toolbar.</span></span> <span data-ttu-id="8c5b9-114">La aplicación puede crear instancias del control arrastrando el control desde la barra de herramientas y colocándolo en un formulario o cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8c5b9-114">Your application can create instances of the control by dragging the control from the toolbar and dropping it onto a form or dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c5b9-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c5b9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c5b9-116">Agregar una referencia a un proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8c5b9-116">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="8c5b9-117">Trasladar a Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8c5b9-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




