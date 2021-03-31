---
title: Trasladar a Visual Basic
description: Trasladar a Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903602"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="1bcc7-103">Trasladar a Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1bcc7-103">Translating to Visual Basic</span></span>

<span data-ttu-id="1bcc7-104">Puede Agregar un objeto COM al proyecto de Visual Basic como una referencia o un componente.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="1bcc7-105">Una vez que el objeto se agrega al proyecto, la aplicación puede tener acceso a sus clases e interfaces.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="1bcc7-106">A continuación, puede utilizar el Examinador de objetos de Visual Basic para ver la información de la biblioteca de tipos del objeto en Visual Basic sintaxis.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="1bcc7-107">Normalmente, los controles se agregan a un proyecto como componentes y los no Controls se agregan como referencias.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="1bcc7-108">Cuando se agrega un objeto COM como componente, aparece en el cuadro de herramientas Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="1bcc7-109">Las nuevas instancias de ese objeto se crean arrastrando el icono del objeto desde el cuadro de herramientas hasta un Visual Basic formulario u otro tipo de contenedor.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="1bcc7-110">Las nuevas instancias de objetos COM agregados como referencias se crean mediante la palabra clave **New** .</span><span class="sxs-lookup"><span data-stu-id="1bcc7-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="1bcc7-111">La distinción entre el uso de una clase como referencia frente a un componente es sutil pero importante.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="1bcc7-112">Cuando se agrega un objeto como referencia, solo se puede usar la biblioteca de tipos que proporciona el control o la biblioteca de tipos "sin procesar".</span><span class="sxs-lookup"><span data-stu-id="1bcc7-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="1bcc7-113">Si agrega un control como componente, Visual Basic combina las propiedades y los métodos del extensor del formulario en el que se incrusta el control con la biblioteca de tipos del control, lo que proporciona una versión ajustada y extendida de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="1bcc7-114">Con esta versión de la biblioteca de tipos, puede usar propiedades de extensor como Top y Left como si formaran parte del control, en lugar del contenedor del control.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="1bcc7-115">En la actualidad, Visual Basic no admite varias bibliotecas de tipos integradas en un único archivo. dll.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="1bcc7-116">Si ejecuta en un archivo DLL que incorpora varias bibliotecas de tipos, debe obtener copias independientes de las bibliotecas de tipos del origen que proporcionó el objeto para poder usar el objeto con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1bcc7-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="1bcc7-117">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="1bcc7-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1bcc7-118">Trasladar a Visual Basic de C++</span><span class="sxs-lookup"><span data-stu-id="1bcc7-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="1bcc7-119">Trasladar a Visual Basic desde Java</span><span class="sxs-lookup"><span data-stu-id="1bcc7-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="1bcc7-120">Agregar un componente a un proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1bcc7-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="1bcc7-121">Agregar una referencia a un proyecto de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1bcc7-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="1bcc7-122">Visual Basic Examinador de objetos</span><span class="sxs-lookup"><span data-stu-id="1bcc7-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="1bcc7-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1bcc7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bcc7-124">Traducir a C++</span><span class="sxs-lookup"><span data-stu-id="1bcc7-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="1bcc7-125">Traducir a Java</span><span class="sxs-lookup"><span data-stu-id="1bcc7-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




