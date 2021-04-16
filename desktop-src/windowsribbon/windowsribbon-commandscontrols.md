---
title: Descripción de los comandos y los controles
description: La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de Windows \ 8212; un sistema basado en un modelo de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Cinta de Windows, información general sobre comandos
- Cinta, información general sobre comandos
- Cinta de Windows, información general sobre controles
- Cinta, información general sobre controles
- sistema de comandos para la cinta de Windows
- controles de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551019"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="fedd9-109">Descripción de los comandos y los controles</span><span class="sxs-lookup"><span data-stu-id="fedd9-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="fedd9-110">La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de Windows, un sistema basado en un modelo de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fedd9-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="fedd9-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="fedd9-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="fedd9-112">Sistema de comandos de la cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="fedd9-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="fedd9-113">Controles</span><span class="sxs-lookup"><span data-stu-id="fedd9-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="fedd9-114">Comandos</span><span class="sxs-lookup"><span data-stu-id="fedd9-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="fedd9-115">La experiencia del comando en acción</span><span class="sxs-lookup"><span data-stu-id="fedd9-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="fedd9-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fedd9-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="fedd9-117">Introducción</span><span class="sxs-lookup"><span data-stu-id="fedd9-117">Introduction</span></span>

<span data-ttu-id="fedd9-118">En este artículo se describe el diseño del sistema de comandos del marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="fedd9-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="fedd9-119">Describe los conceptos de comandos y controles, y explora cómo funcionan conjuntamente para proporcionar una experiencia de comando enriquecida con un host de nuevas capacidades de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fedd9-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="fedd9-120">Sistema de comandos de la cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="fedd9-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="fedd9-121">En el marco de la cinta de opciones, los comandos y los controles son entidades independientes.</span><span class="sxs-lookup"><span data-stu-id="fedd9-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="fedd9-122">Un comando es una estructura abstracta, sin restricciones de presentación, que representa una tarea o clase de funcionalidad específica.</span><span class="sxs-lookup"><span data-stu-id="fedd9-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="fedd9-123">Por otro lado, un control es un objeto concreto que expone la funcionalidad del comando a través de la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="fedd9-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="fedd9-124">Esta distinción proporciona la capacidad de definir comandos que están libres de los detalles de la interfaz de usuario y que pueden ejecutarse en el intento de una acción sin necesidad de administrar cómo se invocó la acción.</span><span class="sxs-lookup"><span data-stu-id="fedd9-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="fedd9-125">Controles</span><span class="sxs-lookup"><span data-stu-id="fedd9-125">Controls</span></span>

<span data-ttu-id="fedd9-126">Los controles son los objetos de interfaz de usuario necesarios para la presentación de comandos.</span><span class="sxs-lookup"><span data-stu-id="fedd9-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="fedd9-127">Se representan y administran en tiempo de ejecución mediante el marco de trabajo en función de la interacción del usuario y un conjunto de propiedades y comportamientos inherentes.</span><span class="sxs-lookup"><span data-stu-id="fedd9-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="fedd9-128">Conocido como diseño adaptable, la flexibilidad administrada por el marco de la interfaz de usuario es una de las grandes ventajas de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="fedd9-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="fedd9-129">Los controles de la cinta de opciones se pueden volver a configurar automáticamente a través de plantillas de diseño dependientes del marco de trabajo o definidas por el desarrollador que pueden responder a diversos requisitos de tiempo de ejecución, todo ello sin escribir una sola línea de código de presentación.</span><span class="sxs-lookup"><span data-stu-id="fedd9-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="fedd9-130">Para obtener más información, vea [personalizar una cinta de opciones a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fedd9-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="fedd9-131">Además de las ventajas del diseño adaptable, una serie de controles de cinta complejos proporcionan soluciones independientes para espacios de la interfaz de usuario específicos.</span><span class="sxs-lookup"><span data-stu-id="fedd9-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="fedd9-132">Al ofrecer un modelo de interacción sofisticado, los controles de la cinta de opciones, como FontControl o ColorPicker, proporcionan la capacidad de manipular datos en términos más abstractos a través de bolsas de propiedades de atributos de fuente o de color reales en lugar de varios subcontrols, enumeraciones y valores de índice de los controles estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="fedd9-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="fedd9-133">Comandos:</span><span class="sxs-lookup"><span data-stu-id="fedd9-133">Commands</span></span>

<span data-ttu-id="fedd9-134">Con un acoplamiento flexible a los controles de la cinta de opciones que exponen su funcionalidad, las implementaciones de comandos son el dominio de la aplicación host y tienen la forma de agentes de escucha de eventos, controladores de comandos y diversas propiedades de comando.</span><span class="sxs-lookup"><span data-stu-id="fedd9-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="fedd9-135">Los comandos se declaran en el marcado de la cinta de opciones con un identificador único o se les asigna un identificador generado por el compilador de marcado en la compilación.</span><span class="sxs-lookup"><span data-stu-id="fedd9-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="fedd9-136">Los comandos se asocian a los controles a través de un nombre de comando, pero, a diferencia de los controles, su funcionalidad real se define en el código donde se enlazan a controladores de comandos concretos mediante el identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="fedd9-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="fedd9-137">En la compilación, este identificador se almacena en un archivo de encabezado de definición de identificador que expone comandos a sus controladores de comandos correspondientes en la aplicación host de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="fedd9-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="fedd9-138">Cada comando tiene un tipo de comando subyacente con elementos en la enumeración [**\_ COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fedd9-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="fedd9-139">La experiencia del comando en acción</span><span class="sxs-lookup"><span data-stu-id="fedd9-139">The Command Experience In Action</span></span>

<span data-ttu-id="fedd9-140">Las capacidades de este modelo de comandos se muestran en la barra de herramientas de acceso rápido de la cinta de opciones (QAT).</span><span class="sxs-lookup"><span data-stu-id="fedd9-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="fedd9-141">QAT proporciona a los usuarios finales una manera fácil de definir sus propios métodos abreviados para prácticamente cualquier control en la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="fedd9-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="fedd9-142">Un acceso directo se agrega dinámicamente al QAT en tiempo de ejecución cuando el usuario hace clic con el botón secundario en un control de la cinta de opciones y selecciona **Agregar a barra de herramientas de acceso rápido** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="fedd9-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="fedd9-143">En la imagen siguiente se muestran los comandos **pegar** y **pegar desde** , representados por un control [**splitButton**](windowsribbon-element-splitbutton.md) , en la cinta de opciones de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="fedd9-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![imagen de pegar splitButton en la cinta de opciones de Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="fedd9-145">En la imagen siguiente se muestran los mismos comandos **pegar** y **pegar desde** , que todavía se representan mediante un control [**splitButton**](windowsribbon-element-splitbutton.md) , en la cinta de opciones Qat de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="fedd9-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![imagen de pegar splitButton en Microsoft Paint Qat.](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="fedd9-147">Cuando un control está hospedado por el QAT, la nueva instancia del control mantiene toda la funcionalidad del control original sin necesidad de que los agentes de escucha de eventos y controladores de comandos adicionales lo admitan.</span><span class="sxs-lookup"><span data-stu-id="fedd9-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="fedd9-148">Ambos controles se enlazan al mismo controlador de comandos de la cinta de opciones a través de un identificador de comando compartido.</span><span class="sxs-lookup"><span data-stu-id="fedd9-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="fedd9-149">De esta manera, el marco de trabajo trata ambos controles como uno, independientemente de lo que se invoca.</span><span class="sxs-lookup"><span data-stu-id="fedd9-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="fedd9-150">Se tienen en cuenta los mismos beneficios cuando los comandos se incorporan en un [**ContextPopup**](windowsribbon-element-contextpopup.md) en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="fedd9-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="fedd9-151">En este caso, se pueden usar los controladores de comandos de pegado si el control [**splitButton**](windowsribbon-element-splitbutton.md) aparece en la cinta de opciones, Qat o **ContextPopup**.</span><span class="sxs-lookup"><span data-stu-id="fedd9-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fedd9-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fedd9-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fedd9-153">Introducción al marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="fedd9-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="fedd9-154">Crear una aplicación de cinta</span><span class="sxs-lookup"><span data-stu-id="fedd9-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="fedd9-155">Declarar comandos y controles con el marcado de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="fedd9-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 