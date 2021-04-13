---
title: Control de fuente
description: Para simplificar la integración y la configuración de la compatibilidad de fuentes en aplicaciones que requieren funciones de procesamiento de texto y de edición de texto, el marco de la cinta de opciones de Windows proporciona un control de fuente especializado que expone una amplia gama de propiedades de fuente como el nombre del tipo de letra, el estilo, el tamaño de los puntos y los efectos.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420972"
---
# <a name="font-control"></a><span data-ttu-id="2bd5c-103">Control de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-103">Font Control</span></span>

<span data-ttu-id="2bd5c-104">Para simplificar la integración y la configuración de la compatibilidad de fuentes en aplicaciones que requieren funciones de procesamiento de texto y de edición de texto, el marco de la cinta de opciones de Windows proporciona un control de fuente especializado que expone una amplia gama de propiedades de fuente como el nombre del tipo de letra, el estilo, el tamaño de los puntos y los efectos.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="2bd5c-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="2bd5c-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="2bd5c-106">Una experiencia coherente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="2bd5c-107">Fácil integración y configuración</span><span class="sxs-lookup"><span data-stu-id="2bd5c-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="2bd5c-108">Alineación con estructuras de texto GDI comunes</span><span class="sxs-lookup"><span data-stu-id="2bd5c-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="2bd5c-109">Agregar un FontControl</span><span class="sxs-lookup"><span data-stu-id="2bd5c-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="2bd5c-110">Declarar un FontControl en el marcado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="2bd5c-111">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="2bd5c-112">Definición de un controlador de comandos de FontControl</span><span class="sxs-lookup"><span data-stu-id="2bd5c-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="2bd5c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bd5c-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="2bd5c-114">Introducción</span><span class="sxs-lookup"><span data-stu-id="2bd5c-114">Introduction</span></span>

<span data-ttu-id="2bd5c-115">El control fuente es un control compuesto que consta de botones, botones de alternancia, cuadros de lista desplegables y cuadros combinados, que se utilizan para especificar una propiedad de fuente o una opción de formato determinadas.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="2bd5c-116">En la captura de pantalla siguiente se muestra el control de fuente de la cinta de opciones en WordPad para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="2bd5c-118">Una experiencia coherente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-118">A Consistent Experience</span></span>

<span data-ttu-id="2bd5c-119">Como control integrado de la cinta de opciones, el control de fuentes mejora la funcionalidad general de administración de fuentes, selección y formato, y proporciona una experiencia de usuario enriquecida y coherente en todas las aplicaciones de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="2bd5c-120">Esta experiencia coherente incluye</span><span class="sxs-lookup"><span data-stu-id="2bd5c-120">This consistent experience includes</span></span>

-   <span data-ttu-id="2bd5c-121">Formato estandarizado y selección de fuentes entre aplicaciones de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="2bd5c-122">Representación de fuentes estandarizada en las aplicaciones de cinta.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="2bd5c-123">Automática, en Windows 7, activación de fuentes basada en el valor **Mostrar** u **ocultar** para cada fuente en el panel de control **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="2bd5c-124">El control fuente solo muestra las fuentes que se han establecido en **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="2bd5c-125">En Windows Vista, el panel de control **fuentes** no ofrece la funcionalidad **Mostrar** u **ocultar** , por lo que se activan todas las fuentes.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="2bd5c-126">Administración de fuentes que está disponible directamente desde el control.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="2bd5c-127">La siguiente captura de pantalla muestra que se puede tener acceso al panel de control **fuentes** directamente desde el control fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![captura de pantalla de la lista de familias de fuentes en WordPad para Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="2bd5c-129">Compatibilidad con la versión preliminar automática.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="2bd5c-130">Exposición de fuentes que son más relevantes para un usuario, como</span><span class="sxs-lookup"><span data-stu-id="2bd5c-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="2bd5c-131">Listas de fuentes localizadas para usuarios internacionales.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="2bd5c-132">Listas de fuentes basadas en el dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="2bd5c-133">La compatibilidad con esta funcionalidad no está disponible en ninguna plataforma anterior a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="2bd5c-134">Fácil integración y configuración</span><span class="sxs-lookup"><span data-stu-id="2bd5c-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="2bd5c-135">Al proporcionar funcionalidad estándar, reutilizable y de uso sencillo, el control de fuente de la cinta facilita la carga de integrar la compatibilidad de fuentes en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="2bd5c-136">Los detalles de la selección de fuentes y el formato se ajustan en uno de los elementos lógicos independientes que</span><span class="sxs-lookup"><span data-stu-id="2bd5c-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="2bd5c-137">Elimina la administración compleja de interdependencias de control típicas de las implementaciones de control de fuentes.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="2bd5c-138">Requiere un solo controlador de comandos para todas las funciones expuestas por los subcontrols de control de fuentes.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="2bd5c-139">Este controlador de comandos único permite al control de fuentes administrar la funcionalidad de varios subcontrols internamente. un subcontrol nunca interactúa directamente con la aplicación, independientemente de su función.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="2bd5c-140">Otras características del control de fuentes incluyen</span><span class="sxs-lookup"><span data-stu-id="2bd5c-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="2bd5c-141">Generación automática con reconocimiento de PPP de una representación de mapa de bits WYSIWYG (lo que se ve es lo que se obtiene) para cada fuente en el menú de la **familia de fuentes** .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="2bd5c-142">Integración de [Windows interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="2bd5c-143">Mapas de bits e información sobre herramientas de la familia de fuentes localizada.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="2bd5c-144">Enumeración de fuentes, agrupación y metadatos para administrar y presentar fuentes.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="2bd5c-145">La compatibilidad con esta funcionalidad no está disponible en ninguna plataforma anterior a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="2bd5c-146">El color del **texto** y el **texto resaltan** los separadores de colores desplegables que reflejan el comportamiento del [selector de colores](windowsribbon-controls-dropdowncolorpicker.md) desplegable de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="2bd5c-147">Compatibilidad con la vista previa automática de todos los subcontrols basados en la galería de controles de fuente: **familia de fuentes**, **tamaño de fuente**, color de **texto** y **color de resaltado de texto**.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="2bd5c-148">Alineación con estructuras de texto GDI comunes</span><span class="sxs-lookup"><span data-stu-id="2bd5c-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="2bd5c-149">Los componentes de la pila de texto de [Windows interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md) se usan para exponer la funcionalidad de selección de fuente y de formato a través del control de fuente de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="2bd5c-150">Las diversas características de fuente admitidas por la estructura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), la [estructura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)y la [estructura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) se exponen a través de los SubControles que se incluyen en el control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="2bd5c-151">Los SubControles que se muestran en el control de fuente dependen de la plantilla *FontType* declarada en el marcado de la cinta.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="2bd5c-152">Las plantillas *FontType* (que se describen con más detalle en la sección siguiente) están diseñadas para alinearse con las estructuras de texto comunes de [Windows interfaz de dispositivo gráfico (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="2bd5c-153">Agregar un FontControl</span><span class="sxs-lookup"><span data-stu-id="2bd5c-153">Add a FontControl</span></span>

<span data-ttu-id="2bd5c-154">En esta sección se describen los pasos básicos para agregar un control de fuente a una aplicación de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="2bd5c-155">Declarar un FontControl en el marcado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="2bd5c-156">Como otros controles de la cinta de opciones, el control de fuente se declara en el marcado con un elemento [**FontControl**](windowsribbon-element-fontcontrol.md) y se asocia a una declaración de comando a través de un identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="2bd5c-157">Cuando se compila la aplicación, el identificador de comando se usa para enlazar el comando a un controlador de comandos en la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="2bd5c-158">Si no se declara ningún identificador de comando con el [**FontControl**](windowsribbon-element-fontcontrol.md) en el marcado, el marco de trabajo genera uno.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="2bd5c-159">Dado que los SubControles del control de fuente no se exponen directamente, la personalización del control de fuente se limita a tres plantillas de diseño de *FontType* definidas por el marco.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="2bd5c-160">La personalización adicional del control de fuente puede realizarse mediante la combinación de la plantilla de diseño con atributos [**FontControl**](windowsribbon-element-fontcontrol.md) como *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* y *IsUnderlineButtonVisible*.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="2bd5c-161">La funcionalidad de fuente más allá de la que exponen las plantillas y atributos del control de fuentes estándar requiere una implementación de control de fuentes personalizada que está fuera del ámbito de este artículo.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="2bd5c-162">En la tabla siguiente se muestran las plantillas de control de fuentes y el tipo de control Edit con el que se alinea cada plantilla.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="2bd5c-163">Plantilla</span><span class="sxs-lookup"><span data-stu-id="2bd5c-163">Template</span></span>      | <span data-ttu-id="2bd5c-164">Es compatible con</span><span class="sxs-lookup"><span data-stu-id="2bd5c-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2bd5c-165">FontOnly</span><span class="sxs-lookup"><span data-stu-id="2bd5c-165">FontOnly</span></span>      | [<span data-ttu-id="2bd5c-166">LOGFONT (estructura)</span><span class="sxs-lookup"><span data-stu-id="2bd5c-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="2bd5c-167">FontWithColor</span><span class="sxs-lookup"><span data-stu-id="2bd5c-167">FontWithColor</span></span> | [<span data-ttu-id="2bd5c-168">Estructura CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="2bd5c-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="2bd5c-169">RichFont</span><span class="sxs-lookup"><span data-stu-id="2bd5c-169">RichFont</span></span>      | [<span data-ttu-id="2bd5c-170">Estructura CHARFORMAT2</span><span class="sxs-lookup"><span data-stu-id="2bd5c-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="2bd5c-171">En la tabla siguiente se enumeran los controles que están asociados a cada plantilla y se identifican los controles que son opcionales para una plantilla asociada.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="2bd5c-172">Controles</span><span class="sxs-lookup"><span data-stu-id="2bd5c-172">Controls</span></span>

<span data-ttu-id="2bd5c-173">Plantillas</span><span class="sxs-lookup"><span data-stu-id="2bd5c-173">Templates</span></span>

<span data-ttu-id="2bd5c-174">**RichFont**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-174">**RichFont**</span></span>

<span data-ttu-id="2bd5c-175">**FontWithColor**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-175">**FontWithColor**</span></span>

<span data-ttu-id="2bd5c-176">**FontOnly**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-176">**FontOnly**</span></span>

<span data-ttu-id="2bd5c-177">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-177">Default</span></span>

<span data-ttu-id="2bd5c-178">Opcional</span><span class="sxs-lookup"><span data-stu-id="2bd5c-178">Optional</span></span>

<span data-ttu-id="2bd5c-179">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-179">Default</span></span>

<span data-ttu-id="2bd5c-180">Opcional</span><span class="sxs-lookup"><span data-stu-id="2bd5c-180">Optional</span></span>

<span data-ttu-id="2bd5c-181">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-181">Default</span></span>

<span data-ttu-id="2bd5c-182">Opcionales</span><span class="sxs-lookup"><span data-stu-id="2bd5c-182">Optional</span></span>

<span data-ttu-id="2bd5c-183">Cuadro combinado de **tamaño de fuente**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-183">**Font size** combo box</span></span>

<span data-ttu-id="2bd5c-184">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-184">Yes</span></span>

<span data-ttu-id="2bd5c-185">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-185">No</span></span>

<span data-ttu-id="2bd5c-186">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-186">Yes</span></span>

<span data-ttu-id="2bd5c-187">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-187">No</span></span>

<span data-ttu-id="2bd5c-188">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-188">Yes</span></span>

<span data-ttu-id="2bd5c-189">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-189">No</span></span>

<span data-ttu-id="2bd5c-190">Cuadro combinado de **familia de fuentes**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-190">**Font family** combo box</span></span>

<span data-ttu-id="2bd5c-191">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-191">Yes</span></span>

<span data-ttu-id="2bd5c-192">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-192">No</span></span>

<span data-ttu-id="2bd5c-193">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-193">Yes</span></span>

<span data-ttu-id="2bd5c-194">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-194">No</span></span>

<span data-ttu-id="2bd5c-195">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-195">Yes</span></span>

<span data-ttu-id="2bd5c-196">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-196">No</span></span>

<span data-ttu-id="2bd5c-197">Botón **aumentar fuente**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-197">**Grow font** button</span></span>

<span data-ttu-id="2bd5c-198">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-198">Yes</span></span>

<span data-ttu-id="2bd5c-199">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-199">Yes</span></span>

<span data-ttu-id="2bd5c-200">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-200">Yes</span></span>

<span data-ttu-id="2bd5c-201">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-201">Yes</span></span>

\-

\-

<span data-ttu-id="2bd5c-202">Botón **reducir fuente**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-202">**Shrink font** button</span></span>

<span data-ttu-id="2bd5c-203">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-203">Yes</span></span>

<span data-ttu-id="2bd5c-204">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-204">Yes</span></span>

<span data-ttu-id="2bd5c-205">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-205">Yes</span></span>

<span data-ttu-id="2bd5c-206">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-206">Yes</span></span>

\-

\-

<span data-ttu-id="2bd5c-207">Botón **negrita**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-207">**Bold** button</span></span>

<span data-ttu-id="2bd5c-208">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-208">Yes</span></span>

<span data-ttu-id="2bd5c-209">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-209">No</span></span>

<span data-ttu-id="2bd5c-210">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-210">Yes</span></span>

<span data-ttu-id="2bd5c-211">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-211">No</span></span>

<span data-ttu-id="2bd5c-212">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-212">Yes</span></span>

<span data-ttu-id="2bd5c-213">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-213">No</span></span>

<span data-ttu-id="2bd5c-214">Botón **cursiva**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-214">**Italic** button</span></span>

<span data-ttu-id="2bd5c-215">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-215">Yes</span></span>

<span data-ttu-id="2bd5c-216">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-216">No</span></span>

<span data-ttu-id="2bd5c-217">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-217">Yes</span></span>

<span data-ttu-id="2bd5c-218">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-218">No</span></span>

<span data-ttu-id="2bd5c-219">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-219">Yes</span></span>

<span data-ttu-id="2bd5c-220">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-220">No</span></span>

<span data-ttu-id="2bd5c-221">**Subrayado** (botón)</span><span class="sxs-lookup"><span data-stu-id="2bd5c-221">**Underline** button</span></span>

<span data-ttu-id="2bd5c-222">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-222">Yes</span></span>

<span data-ttu-id="2bd5c-223">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-223">No</span></span>

<span data-ttu-id="2bd5c-224">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-224">Yes</span></span>

<span data-ttu-id="2bd5c-225">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-225">Yes</span></span>

<span data-ttu-id="2bd5c-226">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-226">Yes</span></span>

<span data-ttu-id="2bd5c-227">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-227">Yes</span></span>

<span data-ttu-id="2bd5c-228">Botón **tachado**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-228">**Strikethrough** button</span></span>

<span data-ttu-id="2bd5c-229">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-229">Yes</span></span>

<span data-ttu-id="2bd5c-230">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-230">No</span></span>

<span data-ttu-id="2bd5c-231">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-231">Yes</span></span>

<span data-ttu-id="2bd5c-232">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-232">Yes</span></span>

<span data-ttu-id="2bd5c-233">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-233">Yes</span></span>

<span data-ttu-id="2bd5c-234">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-234">Yes</span></span>

<span data-ttu-id="2bd5c-235">Botón **subíndice**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-235">**Subscript** button</span></span>

<span data-ttu-id="2bd5c-236">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-236">Yes</span></span>

<span data-ttu-id="2bd5c-237">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="2bd5c-238">Botón **Superscript**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-238">**Superscript** button</span></span>

<span data-ttu-id="2bd5c-239">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-239">Yes</span></span>

<span data-ttu-id="2bd5c-240">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="2bd5c-241">Botón de **color de resaltado de texto**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-241">**Text highlight color** button</span></span>

<span data-ttu-id="2bd5c-242">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-242">Yes</span></span>

<span data-ttu-id="2bd5c-243">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-243">No</span></span>

<span data-ttu-id="2bd5c-244">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-244">Yes</span></span>

<span data-ttu-id="2bd5c-245">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-245">Yes</span></span>

\-

\-

<span data-ttu-id="2bd5c-246">Botón **color del texto**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-246">**Text color** button</span></span>

<span data-ttu-id="2bd5c-247">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-247">Yes</span></span>

<span data-ttu-id="2bd5c-248">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-248">No</span></span>

<span data-ttu-id="2bd5c-249">Sí</span><span class="sxs-lookup"><span data-stu-id="2bd5c-249">Yes</span></span>

<span data-ttu-id="2bd5c-250">No</span><span class="sxs-lookup"><span data-stu-id="2bd5c-250">No</span></span>

\-

\-



 

<span data-ttu-id="2bd5c-251">Cuando se declara el comportamiento de diseño de un control de fuente, el marco de la cinta de opciones proporciona una plantilla de diseño *SizeDefinition* opcional, `OneFontControl` , que define dos configuraciones de subcontrol basadas en el tamaño de la cinta de opciones y el espacio disponible para el control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="2bd5c-252">Para obtener más información, vea [personalizar una cinta de opciones a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="2bd5c-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="2bd5c-253">Agregar un FontControl a una cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="2bd5c-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="2bd5c-254">En los siguientes ejemplos de código se muestran los requisitos básicos de marcado para agregar un control de fuente a una cinta de opciones:</span><span class="sxs-lookup"><span data-stu-id="2bd5c-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="2bd5c-255">En esta sección de código se muestra el marcado de declaración del comando [**FontControl**](windowsribbon-element-fontcontrol.md) , incluidos los comandos de [**pestaña**](windowsribbon-element-tab.md) y de [**Grupo**](windowsribbon-element-group.md) necesarios para mostrar un control en la [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="2bd5c-256">En esta sección de código se muestra el marcado necesario para declarar y asociar un [**FontControl**](windowsribbon-element-fontcontrol.md) con un [**comando**](windowsribbon-element-command.md) mediante un identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="2bd5c-257">En este ejemplo concreto se incluyen las declaraciones de [**pestaña**](windowsribbon-element-tab.md) y [**Grupo**](windowsribbon-element-group.md) , con las preferencias de escalado.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="2bd5c-258">Agregar un FontControl a un ContextPopup</span><span class="sxs-lookup"><span data-stu-id="2bd5c-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="2bd5c-259">Agregar un control de fuente a un [elemento emergente de contexto](windowsribbon-controls-contextpopup.md) requiere un procedimiento similar al de agregar un control de fuente a la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="2bd5c-260">Sin embargo, un control de fuente de un [**MiniToolbar**](windowsribbon-element-minitoolbar.md) está restringido al conjunto de subcontrols predeterminados que son comunes a todas las plantillas de control de fuentes: **familia de fuentes**, **tamaño de fuente**, **negrita** y **cursiva**.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="2bd5c-261">En los siguientes ejemplos de código se muestran los requisitos básicos de marcado para agregar un control de fuente a un [elemento emergente de contexto](windowsribbon-controls-contextpopup.md):</span><span class="sxs-lookup"><span data-stu-id="2bd5c-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="2bd5c-262">En esta sección de código se muestra el marcado de declaración de comandos [**FontControl**](windowsribbon-element-fontcontrol.md) que se requiere para mostrar un **FontControl** en [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="2bd5c-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="2bd5c-263">En esta sección de código se muestra el marcado necesario para declarar y asociar un [**FontControl**](windowsribbon-element-fontcontrol.md) con un comando mediante un identificador de comando.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="2bd5c-264">Keytips</span><span class="sxs-lookup"><span data-stu-id="2bd5c-264">Keytips</span></span>

<span data-ttu-id="2bd5c-265">Cada subcontrol del control de fuente de la cinta de opciones es accesible a través de un método abreviado de teclado o KeyTip.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="2bd5c-266">Este KeyTip está predefinido y se asigna a cada subcontrol por el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="2bd5c-267">Si se asigna un valor de atributo *KeyTip* al elemento [**FontControl**](windowsribbon-element-fontcontrol.md) en el marcado, este valor se agrega como prefijo al KeyTip definido por el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="2bd5c-268">La aplicación debe aplicar una regla de un solo carácter para este prefijo.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="2bd5c-269">En la tabla siguiente se enumeran las keytips definidas por el marco.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd5c-270">Control secundario</span><span class="sxs-lookup"><span data-stu-id="2bd5c-270">Sub-control</span></span></th>
<th><span data-ttu-id="2bd5c-271">KeyTip</span><span class="sxs-lookup"><span data-stu-id="2bd5c-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bd5c-272">Familia de fuentes</span><span class="sxs-lookup"><span data-stu-id="2bd5c-272">Font family</span></span></td>
<td><span data-ttu-id="2bd5c-273">F</span><span class="sxs-lookup"><span data-stu-id="2bd5c-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd5c-274">Estilo de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-274">Font style</span></span></td>
<td><span data-ttu-id="2bd5c-275">T</span><span class="sxs-lookup"><span data-stu-id="2bd5c-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd5c-276">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-276">Font size</span></span></td>
<td><span data-ttu-id="2bd5c-277">S</span><span class="sxs-lookup"><span data-stu-id="2bd5c-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd5c-278">Aumentar fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-278">Grow font</span></span></td>
<td><span data-ttu-id="2bd5c-279">G</span><span class="sxs-lookup"><span data-stu-id="2bd5c-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd5c-280">Reducir fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-280">Shrink font</span></span></td>
<td><span data-ttu-id="2bd5c-281">K</span><span class="sxs-lookup"><span data-stu-id="2bd5c-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd5c-282">Bold</span><span class="sxs-lookup"><span data-stu-id="2bd5c-282">Bold</span></span></td>
<td><span data-ttu-id="2bd5c-283">B</span><span class="sxs-lookup"><span data-stu-id="2bd5c-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd5c-284">Cursiva</span><span class="sxs-lookup"><span data-stu-id="2bd5c-284">Italic</span></span></td>
<td><span data-ttu-id="2bd5c-285">I</span><span class="sxs-lookup"><span data-stu-id="2bd5c-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd5c-286">Subrayado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-286">Underline</span></span></td>
<td><span data-ttu-id="2bd5c-287">U</span><span class="sxs-lookup"><span data-stu-id="2bd5c-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd5c-288">Tachado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-288">Strikethrough</span></span></td>
<td><span data-ttu-id="2bd5c-289">X</span><span class="sxs-lookup"><span data-stu-id="2bd5c-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd5c-290">Superscript</span><span class="sxs-lookup"><span data-stu-id="2bd5c-290">Superscript</span></span></td>
<td><span data-ttu-id="2bd5c-291">Y o Z</span><span class="sxs-lookup"><span data-stu-id="2bd5c-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bd5c-292">Si el atributo <em>KeyTip</em> no se declara en el marcado, el KeyTip predeterminado es Y; de lo contrario, el KeyTip predeterminado es <em>KeyTip</em> + Z.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd5c-293">Subscript</span><span class="sxs-lookup"><span data-stu-id="2bd5c-293">Subscript</span></span></td>
<td><span data-ttu-id="2bd5c-294">A</span><span class="sxs-lookup"><span data-stu-id="2bd5c-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bd5c-295">Color de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-295">Font color</span></span></td>
<td><span data-ttu-id="2bd5c-296">C</span><span class="sxs-lookup"><span data-stu-id="2bd5c-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bd5c-297">Resaltado de fuentes</span><span class="sxs-lookup"><span data-stu-id="2bd5c-297">Font highlight</span></span></td>
<td><span data-ttu-id="2bd5c-298">H</span><span class="sxs-lookup"><span data-stu-id="2bd5c-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2bd5c-299">El prefijo recomendado para una interfaz de usuario multilingüe (MUI) EN-US es "F", tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="2bd5c-300">En la siguiente captura de pantalla se muestran las keytips del control de fuentes, tal como se definen en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![captura de pantalla de las keytips de fontcontrol en WordPad para Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="2bd5c-302">El archivo de recursos de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="2bd5c-302">The Ribbon Resource File</span></span>

<span data-ttu-id="2bd5c-303">Cuando se compila el archivo de marcado, se genera un archivo de recursos que contiene todas las referencias de recursos para la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="2bd5c-304">Ejemplo de un archivo de recursos simple:</span><span class="sxs-lookup"><span data-stu-id="2bd5c-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="2bd5c-305">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-305">Font Control Properties</span></span>

<span data-ttu-id="2bd5c-306">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de fuente y sus subcontrols constituyentes.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="2bd5c-307">Normalmente, una propiedad de control de fuente se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2bd5c-308">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2bd5c-309">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2bd5c-310">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2bd5c-311">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2bd5c-312">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="2bd5c-313">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="2bd5c-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="2bd5c-314">Notas</span><span class="sxs-lookup"><span data-stu-id="2bd5c-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bd5c-315">UI \_ PKEY \_ FontProperties</span><span class="sxs-lookup"><span data-stu-id="2bd5c-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="2bd5c-316">Expone, en Aggregate como un objeto [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , todas las propiedades de subcontrol de control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="2bd5c-317">El marco de trabajo consulta esta propiedad cuando `UI_INVALIDATIONS_VALUE` se pasa como el valor de *Flags* en la llamada a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="2bd5c-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="2bd5c-318">UI \_ PKEY \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="2bd5c-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="2bd5c-319">Expone, en Aggregate como un objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , solo las propiedades de subcontrol de control de fuente que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="2bd5c-320">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="2bd5c-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="2bd5c-321">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2bd5c-322">PKEY de IU \_ \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="2bd5c-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="2bd5c-323">Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="2bd5c-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="2bd5c-324">Además de las propiedades admitidas por el propio control de fuente, el marco de la cinta de opciones también define una [clave de propiedad](windowsribbon-reference-properties.md) para cada subcontrol de control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="2bd5c-325">El marco de trabajo expone estas claves de propiedad y sus valores a través de una implementación de la interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que define los métodos para administrar una colección, también denominada bolsa de propiedades, de pares nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="2bd5c-326">La aplicación traduce las estructuras de fuente a propiedades a las que se puede tener acceso a través de los métodos de la interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="2bd5c-327">Este modelo resalta la distinción entre el control de fuente y los componentes de la pila de texto de Windows Interfaz de dispositivo gráfico (GDI) ([estructura LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [estructura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)y [estructura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) que son compatibles con el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="2bd5c-328">En la tabla siguiente se enumeran los controles individuales y sus claves de propiedad asociadas.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="2bd5c-329">Controles</span><span class="sxs-lookup"><span data-stu-id="2bd5c-329">Controls</span></span>                 | <span data-ttu-id="2bd5c-330">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="2bd5c-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="2bd5c-331">Notas</span><span class="sxs-lookup"><span data-stu-id="2bd5c-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd5c-332">**Tamaño de fuente**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-332">**Font size**</span></span>            | [<span data-ttu-id="2bd5c-333">Tamaño de FontProperties de UI \_ PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd5c-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="2bd5c-334">Cuando se resalta una ejecución de texto de tamaño heterogéneo, el marco de la cinta de opciones establece el control de **tamaño de fuente** en Blank y el valor de la [interfaz de usuario \_ PKEY \_ FontProperties \_ size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) en 0.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="2bd5c-335">Cuando se hace clic en el botón **aumentar fuente** o **reducir fuente** , se cambia el tamaño de todo el texto resaltado, pero se conserva la diferencia relativa en los tamaños de texto.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="2bd5c-336">**Familia de fuentes**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-336">**Font family**</span></span>          | [<span data-ttu-id="2bd5c-337">Familia de FontProperties de UI \_ PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd5c-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="2bd5c-338">Los nombres de familia de fuentes de GDI varían con la configuración regional del sistema.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="2bd5c-339">Por lo tanto, si el valor de la [familia de PKEY de interfaz de usuario \_ \_ FontProperties \_ ](windowsribbon-reference-properties-uipkey-fontproperties-family.md) se conserva en las sesiones de la aplicación, ese valor se debe recuperar en cada nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2bd5c-340">**Aumentar fuente**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-340">**Grow font**</span></span>            | [<span data-ttu-id="2bd5c-341">Tamaño de FontProperties de UI \_ PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd5c-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="2bd5c-342">Vea **tamaño de fuente**.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2bd5c-343">**Reducir fuente**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-343">**Shrink font**</span></span>          | [<span data-ttu-id="2bd5c-344">Tamaño de FontProperties de UI \_ PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd5c-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="2bd5c-345">Vea **tamaño de fuente**.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2bd5c-346">**Negrita**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-346">**Bold**</span></span>                 | [<span data-ttu-id="2bd5c-347">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="2bd5c-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2bd5c-348">**Cursiva**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-348">**Italic**</span></span>               | [<span data-ttu-id="2bd5c-349">UI \_ PKEY \_ FontProperties \_ cursiva</span><span class="sxs-lookup"><span data-stu-id="2bd5c-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2bd5c-350">**Raya**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-350">**Underline**</span></span>            | [<span data-ttu-id="2bd5c-351">Subrayado de UI \_ PKEY \_ FontProperties \_</span><span class="sxs-lookup"><span data-stu-id="2bd5c-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2bd5c-352">**Tachado**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-352">**Strikethrough**</span></span>        | [<span data-ttu-id="2bd5c-353">PKEY de IU \_ \_ FontProperties \_ tachado</span><span class="sxs-lookup"><span data-stu-id="2bd5c-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2bd5c-354">**Subíndice**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-354">**Subscript**</span></span>            | [<span data-ttu-id="2bd5c-355">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="2bd5c-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="2bd5c-356">Si se establece el botón **subíndice** , no se puede establecer también el **superíndice** .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2bd5c-357">**Superscript**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-357">**Superscript**</span></span>          | [<span data-ttu-id="2bd5c-358">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="2bd5c-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="2bd5c-359">Si se establece el botón de **superíndice** , no se puede establecer también el **subíndice** .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2bd5c-360">**Color de resaltado de texto**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-360">**Text highlight color**</span></span> | <span data-ttu-id="2bd5c-361">[Interfaz de usuario \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ PKEY \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="2bd5c-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="2bd5c-362">Proporciona la misma funcionalidad que la `HighlightColors` plantilla del elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="2bd5c-363">Es muy recomendable que la aplicación solo establezca un valor de **color de resaltado de texto** inicial.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="2bd5c-364">El último valor seleccionado debe conservarse y no establecerse cuando el cursor se cambie de posición dentro de un documento.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="2bd5c-365">Esto permite un acceso rápido a la última selección del usuario y no es necesario volver a abrir el selector de colores.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="2bd5c-366">Las muestras de colores no se pueden personalizar.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="2bd5c-367">**Color del texto**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-367">**Text color**</span></span>           | <span data-ttu-id="2bd5c-368">[Interfaz de usuario \_ PKEY \_ FontProperties \_ foregroundcolor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ PKEY \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="2bd5c-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="2bd5c-369">Proporciona la misma funcionalidad que la `StandardColors` plantilla del elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd5c-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="2bd5c-370">Es muy recomendable que la aplicación solo establezca un valor de **color de texto** inicial.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="2bd5c-371">El último valor seleccionado debe conservarse y no establecerse cuando el cursor se cambie de posición dentro de un documento.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="2bd5c-372">Esto permite un acceso rápido a la última selección del usuario y no es necesario volver a abrir el selector de colores.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="2bd5c-373">Las muestras de colores no se pueden personalizar.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="2bd5c-374">Definición de un controlador de comandos de FontControl</span><span class="sxs-lookup"><span data-stu-id="2bd5c-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="2bd5c-375">En esta sección se describen los pasos necesarios para enlazar un control de fuente a un controlador de comandos.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="2bd5c-376">Cualquier intento de seleccionar una muestra de color del selector de colores de un control de fuente puede producir una infracción de acceso si no hay ningún controlador de comandos asociado al control.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="2bd5c-377">En el ejemplo de código siguiente se muestra cómo enlazar comandos que se declaran en el marcado a un controlador de comandos.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="2bd5c-378">En el ejemplo de código siguiente se muestra cómo implementar el método [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para un control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="2bd5c-379">En el ejemplo de código siguiente se muestra cómo implementar el método [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) para un control de fuente.</span><span class="sxs-lookup"><span data-stu-id="2bd5c-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2bd5c-380">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bd5c-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd5c-381">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="2bd5c-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2bd5c-382">**Elemento FontControl**</span><span class="sxs-lookup"><span data-stu-id="2bd5c-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="2bd5c-383">Propiedades de control de fuente</span><span class="sxs-lookup"><span data-stu-id="2bd5c-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="2bd5c-384">Ejemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="2bd5c-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

