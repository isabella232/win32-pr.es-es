---
title: Guías para desarrolladores del marco de cinta de Windows
description: Los temas incluidos en esta sección describen aspectos específicos del marco de la cinta de opciones de Windows.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Cinta de Windows, marco
- Cinta de opciones, marco
- Cinta de opciones de Windows, guías para desarrolladores
- Cinta de opciones, guías para desarrolladores
- guías del desarrollador para la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149531"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="f5697-108">Guías para desarrolladores del marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="f5697-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="f5697-109">Los temas incluidos en esta sección describen aspectos específicos del marco de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="f5697-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="f5697-110">Aspectos básicos</span><span class="sxs-lookup"><span data-stu-id="f5697-110">Basics</span></span>

[<span data-ttu-id="f5697-111">Crear una aplicación de cinta</span><span class="sxs-lookup"><span data-stu-id="f5697-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="f5697-112">Para que el marco de la cinta de opciones de Windows consuma el archivo de marcado de la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario.</span><span class="sxs-lookup"><span data-stu-id="f5697-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="f5697-113">Un compilador de marcado de cinta dedicado, el compilador de comandos de interfaz de usuario (UICC), se incluye en el kit de desarrollo de software (SDK) de Microsoft Windows (7,0 o posterior) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="f5697-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="f5697-114">Además de compilar la versión binaria del marcado de la cinta, UICC genera un archivo de encabezado de definición de identificador (. h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (. RC) que se usa para vincular los recursos de imagen y de cadena a la aplicación host en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="f5697-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="f5697-115">Migrar al marco de cinta de Windows</span><span class="sxs-lookup"><span data-stu-id="f5697-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="f5697-116">Una aplicación que se basa en los menús, las barras de herramientas y los cuadros de diálogo tradicionales se puede migrar a la interfaz de usuario (UI) enriquecida, dinámica y controlada por el contexto del sistema de comandos del marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="f5697-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="f5697-117">Esta es una manera fácil y eficaz de modernizar y revitalizar la aplicación, a la vez que mejora la accesibilidad, la facilidad de uso y la capacidad de detección de su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="f5697-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="f5697-118">Descripción de los comandos y los controles</span><span class="sxs-lookup"><span data-stu-id="f5697-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="f5697-119">La separación de la lógica de la presentación es la filosofía de diseño que inspira el sistema de presentación de comandos del marco de la cinta de opciones, un sistema basado en un modelo de diseño donde la funcionalidad y el comportamiento se implementan independientemente de los controles que exponen esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="f5697-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="f5697-120">Interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f5697-120">User Interface</span></span>

[<span data-ttu-id="f5697-121">Especificar recursos de imagen de cinta</span><span class="sxs-lookup"><span data-stu-id="f5697-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="f5697-122">Como sistema de presentación de comandos enriquecido, el marco de la cinta de opciones se ha diseñado para admitir los recursos de imagen en gran medida a través de la interfaz de usuario (UI) de la cinta.</span><span class="sxs-lookup"><span data-stu-id="f5697-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="f5697-123">Todos los recursos de imagen se declaran en el [marcado de la cinta](windowsribbon-schema.md) o se consultan desde una aplicación host de cinta.</span><span class="sxs-lookup"><span data-stu-id="f5697-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="f5697-124">En Windows 8 y versiones posteriores, el marco de la cinta de opciones admite los siguientes formatos de gráficos: archivos de mapa de bits ARGB de 32 bits (BMP) y archivos PNG (Portable Network Graphics) con transparencia.</span><span class="sxs-lookup"><span data-stu-id="f5697-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="f5697-125">En Windows 7 y versiones anteriores, los recursos de imagen deben ajustarse al formato de gráficos BMP estándar usado en Windows.</span><span class="sxs-lookup"><span data-stu-id="f5697-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="f5697-126">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="f5697-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="f5697-127">Los controles hospedados en la barra de comandos de la cinta están sujetos a las reglas de diseño que aplica el marco de la cinta de opciones y en función de una combinación de comportamientos y plantillas de diseño predeterminados (definidas por el marco y personalizadas) como se declara en el marcado de la cinta.</span><span class="sxs-lookup"><span data-stu-id="f5697-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="f5697-128">Estas reglas definen los comportamientos de diseño adaptable del marco de cinta que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f5697-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="f5697-129">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="f5697-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="f5697-130">El marco de la cinta de opciones proporciona a los desarrolladores un modelo sólido y coherente para administrar el contenido dinámico en diversos controles basados en colecciones.</span><span class="sxs-lookup"><span data-stu-id="f5697-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="f5697-131">Al adaptar y volver a configurar la interfaz de usuario de la cinta de opciones, estos controles dinámicos permiten que el marco de trabajo responda a la interacción del usuario en la propia cinta y la aplicación host, y proporciona la flexibilidad necesaria para controlar diversos entornos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f5697-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="f5697-132">Mostrar pestañas contextuales</span><span class="sxs-lookup"><span data-stu-id="f5697-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="f5697-133">En una aplicación de marco de cinta, una pestaña contextual es un control de [pestaña](windowsribbon-controls-tab.md) oculto que se muestra en la fila de pestañas cuando se selecciona o resalta un objeto en el área de trabajo de la aplicación, como una imagen.</span><span class="sxs-lookup"><span data-stu-id="f5697-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="f5697-134">Volver a configurar la cinta de opciones con modos de aplicación</span><span class="sxs-lookup"><span data-stu-id="f5697-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="f5697-135">El marco de la cinta de opciones admite la reconfiguración dinámica y la exposición de los elementos básicos de la interfaz de usuario (UI) de la cinta en tiempo de ejecución, en función del estado de la aplicación (también conocido como contexto).</span><span class="sxs-lookup"><span data-stu-id="f5697-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="f5697-136">Declarado y asociado con elementos específicos en el marcado, los distintos Estados admitidos por una aplicación se conocen como modos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5697-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="f5697-137">Personalizar los colores de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f5697-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="f5697-138">El marco de la cinta de opciones expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario (UI) de la cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f5697-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="f5697-139">Mostrar la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f5697-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="f5697-140">El marco de la cinta de opciones expone un conjunto de propiedades que permiten a una aplicación especificar cómo se muestra la interfaz de usuario (UI) de la cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f5697-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="f5697-141">Administración</span><span class="sxs-lookup"><span data-stu-id="f5697-141">Management</span></span>

[<span data-ttu-id="f5697-142">Conservar el estado de la cinta</span><span class="sxs-lookup"><span data-stu-id="f5697-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="f5697-143">Windows Ribon Framework (cinta) ofrece la posibilidad de conservar el estado de una variedad de configuraciones y preferencias de usuario en las sesiones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5697-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="f5697-144">Escuchar eventos de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f5697-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="f5697-145">El marco de la cinta de opciones usa la infraestructura [de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para que los desarrolladores puedan saber cómo interactúan los usuarios con la cinta de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f5697-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="f5697-146">Compilador de marcado</span><span class="sxs-lookup"><span data-stu-id="f5697-146">Markup Compiler</span></span>

[<span data-ttu-id="f5697-147">Compilar marcado de cinta</span><span class="sxs-lookup"><span data-stu-id="f5697-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="f5697-148">Para que el marco de cinta utilice el archivo de marcado de la [cinta](windowsribbon-schema.md) de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario.</span><span class="sxs-lookup"><span data-stu-id="f5697-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="f5697-149">Un compilador de marcado dedicado, el compilador de comandos de la interfaz de usuario (UICC), se incluye con el kit de desarrollo de software (SDK) de Microsoft Windows (SDK) (7,0 o posterior) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="f5697-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="f5697-150">Además de compilar la versión binaria del marcado, UICC genera un archivo de encabezado de definición de identificador (. h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (. RC) que se usa para vincular los recursos de imagen y de cadena a la aplicación host en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="f5697-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="f5697-151">Descripción de los mensajes del compilador de marcado</span><span class="sxs-lookup"><span data-stu-id="f5697-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="f5697-152">El compilador de marcado de Windows Ribbon Framework (cinta), el compilador de comandos de la interfaz de usuario (UICC.exe), valida el marcado de la cinta de opciones con el esquema de la cinta de opciones y un conjunto adicional de reglas definido por el marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="f5697-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 