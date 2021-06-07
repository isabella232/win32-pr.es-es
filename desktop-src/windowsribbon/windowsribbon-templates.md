---
title: Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado
description: Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a reglas de diseño que exige el marco de la cinta de opciones de Windows y se basan en una combinación de comportamientos predeterminados y plantillas de diseño (tanto definidas como personalizadas por el marco) tal y como se declara en el marcado de la cinta de opciones. Estas reglas definen los comportamientos de diseño adaptable del marco de la cinta de opciones que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Cinta de opciones de Windows, personalización
- Cinta de opciones, personalización
- Cinta de opciones de Windows, plantillas SizeDefinition
- Ribbon,SizeDefinition templates
- Cinta de opciones de Windows, plantillas personalizadas
- Cinta de opciones, plantillas personalizadas
- personalizar la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444146"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="221c8-111">Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="221c8-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="221c8-112">Los controles hospedados en la barra de comandos de la cinta de opciones están sujetos a reglas de diseño que exige el marco de la cinta de opciones de Windows y se basan en una combinación de comportamientos predeterminados y plantillas de diseño (tanto definidas como personalizadas por el marco) tal y como se declara en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="221c8-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="221c8-113">Estas reglas definen los comportamientos de diseño adaptable del marco de la cinta de opciones que influyen en cómo se adaptan los controles de la barra de comandos a varios tamaños de cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="221c8-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="221c8-114">Introducción</span><span class="sxs-lookup"><span data-stu-id="221c8-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="221c8-115">Plantillas SizeDefinition de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="221c8-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="221c8-116">Plantillas personalizadas</span><span class="sxs-lookup"><span data-stu-id="221c8-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="221c8-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="221c8-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="221c8-118">Introducción</span><span class="sxs-lookup"><span data-stu-id="221c8-118">Introduction</span></span>

<span data-ttu-id="221c8-119">El diseño adaptable, tal como se define en el marco de la cinta de opciones, es la capacidad de todos los controles dentro de la interfaz de usuario de la cinta de opciones de ajustar dinámicamente su organización, tamaño, formato y escala relativa en función de los cambios en el tamaño de la cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="221c8-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="221c8-120">El marco expone la funcionalidad de diseño adaptable a través de un conjunto de elementos de marcado dedicados a especificar y personalizar varios comportamientos de diseño.</span><span class="sxs-lookup"><span data-stu-id="221c8-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="221c8-121">El marco define una colección de plantillas, [**denominada SizeDefinitions,**](windowsribbon-element-sizedefinition.md)cada una de las cuales admite varios escenarios de control y diseño.</span><span class="sxs-lookup"><span data-stu-id="221c8-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="221c8-122">Sin embargo, el marco también admite plantillas personalizadas si las plantillas predefinidas no proporcionan la experiencia de interfaz de usuario o los diseños requeridos por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="221c8-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="221c8-123">Para mostrar controles en un diseño preferido con un tamaño de cinta determinado, tanto las plantillas predefinidas como las plantillas personalizadas funcionan junto con el [**elemento ScalingPolicy.**](windowsribbon-element-scalingpolicy.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="221c8-124">Este elemento contiene un manifiesto de preferencias de tamaño que el marco usa como guía al representar la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="221c8-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="221c8-125">El marco de la cinta de opciones proporciona comportamientos de diseño predeterminados basados en un conjunto de heurística integrada para la organización y la presentación de controles en tiempo de ejecución sin necesidad de las plantillas [**Predefinidas sizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="221c8-126">Sin embargo, esta funcionalidad está pensada solo para fines de creación de prototipos.</span><span class="sxs-lookup"><span data-stu-id="221c8-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="221c8-127">Plantillas SizeDefinition de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="221c8-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="221c8-128">El marco de la cinta de opciones proporciona un conjunto completo de [**plantillas SizeDefinition**](windowsribbon-element-sizedefinition.md) que especifican el tamaño y el comportamiento de diseño para un [grupo de](windowsribbon-controls-group.md) controles de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="221c8-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="221c8-129">Estas plantillas cubren los escenarios más comunes para organizar controles en una aplicación de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="221c8-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="221c8-130">Para aplicar una experiencia de usuario coherente en las aplicaciones de la cinta de opciones, cada plantilla [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restricciones en los controles o en la familia de controles que admite.</span><span class="sxs-lookup"><span data-stu-id="221c8-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="221c8-131">Por ejemplo, la familia de botones de controles incluye:</span><span class="sxs-lookup"><span data-stu-id="221c8-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="221c8-132">Button</span><span class="sxs-lookup"><span data-stu-id="221c8-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="221c8-133">Botón De alternancia</span><span class="sxs-lookup"><span data-stu-id="221c8-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="221c8-134">Botón desplegable</span><span class="sxs-lookup"><span data-stu-id="221c8-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="221c8-135">Botón De división</span><span class="sxs-lookup"><span data-stu-id="221c8-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="221c8-136">Galería desplegable</span><span class="sxs-lookup"><span data-stu-id="221c8-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="221c8-137">Galería de botones de división</span><span class="sxs-lookup"><span data-stu-id="221c8-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="221c8-138">Lista desplegable Selector de colores</span><span class="sxs-lookup"><span data-stu-id="221c8-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="221c8-139">Mientras que la familia de entrada de controles incluye:</span><span class="sxs-lookup"><span data-stu-id="221c8-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="221c8-140">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="221c8-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="221c8-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="221c8-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="221c8-142">[Las casillas](windowsribbon-controls-checkbox.md) [y la](windowsribbon-controls-inribbongallery.md) Galería de la cinta de opciones no pertenecen a la familia de botones ni a la familia de entrada.</span><span class="sxs-lookup"><span data-stu-id="221c8-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="221c8-143">Estos dos controles solo se pueden usar cuando se indica explícitamente en una [**plantilla SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="221c8-144">A continuación se muestra una lista de las [**plantillas SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descripción del diseño y los controles permitidos por cada plantilla.</span><span class="sxs-lookup"><span data-stu-id="221c8-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="221c8-145">Si los controles declarados en el marcado no se asignan exactamente al tipo de control, el [](windowsribbon-intentcl.md) orden y la cantidad definidos en la plantilla asociada, el compilador de marcado registra un [error](windowsribbon-compilationerrors.md) de validación y finaliza la compilación.</span><span class="sxs-lookup"><span data-stu-id="221c8-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="221c8-146">Onebutton</span><span class="sxs-lookup"><span data-stu-id="221c8-146">OneButton</span></span>

<span data-ttu-id="221c8-147">Un control de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-147">One button-family control.</span></span><br/> <span data-ttu-id="221c8-148">Solo se admite el tamaño de grupo grande.</span><span class="sxs-lookup"><span data-stu-id="221c8-148">Only Large group size is supported.</span></span><br/>

![imagen de la plantilla onebutton sizedefinition.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="221c8-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-150">TwoButtons</span></span>

<span data-ttu-id="221c8-151">Dos controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-151">Two button-family controls.</span></span><br/> <span data-ttu-id="221c8-152">Solo se admiten tamaños de grupo grandes y medianos.</span><span class="sxs-lookup"><span data-stu-id="221c8-152">Only Large and Medium group sizes are supported.</span></span><br/>

![imagen de la plantilla twobuttons large sizedefinition.](images/overviews/sizedefinition-twobuttons-large.png)

![imagen de la plantilla twobuttons medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="221c8-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-155">ThreeButtons</span></span>

<span data-ttu-id="221c8-156">Tres controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-156">Three button-family controls.</span></span><br/> <span data-ttu-id="221c8-157">Solo se admiten tamaños de grupo grandes y medianos.</span><span class="sxs-lookup"><span data-stu-id="221c8-157">Only Large and Medium group sizes are supported.</span></span><br/>

![imagen de la plantilla de definición de tamaño grande de tres botones.](images/overviews/sizedefinition-threebuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de tres botones.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="221c8-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="221c8-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="221c8-161">Tres controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-161">Three button-family controls.</span></span><br/> <span data-ttu-id="221c8-162">El primer botón se presenta de forma destacada en los tres tamaños.</span><span class="sxs-lookup"><span data-stu-id="221c8-162">The first button is presented prominently in all three sizes.</span></span><br/>

![imagen de la plantilla threebuttons-onebigandtwosmall large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![imagen de la plantilla threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![imagen de la plantilla threebuttons-onebigandtwosmall small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="221c8-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="221c8-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="221c8-167">Tres controles de familia de botones acompañados de un único control CheckBox.</span><span class="sxs-lookup"><span data-stu-id="221c8-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="221c8-168">Solo se admiten tamaños de grupo grandes y medianos.</span><span class="sxs-lookup"><span data-stu-id="221c8-168">Only Large and Medium group sizes are supported.</span></span><br/>

![imagen de la plantilla threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![imagen de la plantilla threebuttonsandonecheckbox medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="221c8-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-171">FourButtons</span></span>

<span data-ttu-id="221c8-172">Cuatro controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-172">Four button-family controls.</span></span><br/>

![imagen de la plantilla de definición de tamaño grande de cuatro botones.](images/overviews/sizedefinition-fourbuttons-large.png)

![imagen de la plantilla fourbuttons medium sizedefinition.](images/overviews/sizedefinition-fourbuttons-medium.png)

![imagen de la plantilla sizedefinition de cuatro botones pequeños.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="221c8-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-176">FiveButtons</span></span>

<span data-ttu-id="221c8-177">Cinco controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-177">Five button-family controls.</span></span><br/>

![imagen de la plantilla de definición de tamaño grande de cinco botones.](images/overviews/sizedefinition-fivebuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de cinco botones.](images/overviews/sizedefinition-fivebuttons-medium.png)

![imagen de la plantilla small sizedefinition de cinco botones.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="221c8-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-181">FiveOrSixButtons</span></span>

<span data-ttu-id="221c8-182">Cinco controles de familia de botones y un sexto botón opcional.</span><span class="sxs-lookup"><span data-stu-id="221c8-182">Five button-family controls and an optional sixth button.</span></span><br/>

![imagen de la plantilla fiveorsixbuttons large sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![imagen de la plantilla fiveorsixbuttons medium sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![imagen de la plantilla fiveorsixbuttons small sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="221c8-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-186">SixButtons</span></span>

<span data-ttu-id="221c8-187">Seis controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-187">Six button-family controls.</span></span><br/>

![imagen de la plantilla de definición de tamaño grande de seis botones.](images/overviews/sizedefinition-sixbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de seis botones.](images/overviews/sizedefinition-sixbuttons-medium.png)

![imagen de la plantilla de definición de tamaño pequeño de seis botones.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="221c8-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="221c8-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="221c8-192">Seis controles de familia de botones (presentación alternativa).</span><span class="sxs-lookup"><span data-stu-id="221c8-192">Six button-family controls (alternate presentation).</span></span><br/>

![imagen de la plantilla sixbuttons-twocolumns large sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![Plantilla sixbuttons-twocolumns medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![imagen de la plantilla de definición de tamaño pequeño sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="221c8-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-196">SevenButtons</span></span>

<span data-ttu-id="221c8-197">Siete controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-197">Seven button-family controls.</span></span><br/>

![imagen de la plantilla de definición de tamaño grande de siete botones.](images/overviews/sizedefinition-sevenbuttons-large.png)

![imagen de la plantilla de definición mediumsize de siete botones.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![imagen de la plantilla de definición de tamaño pequeño de siete botones.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="221c8-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-201">EightButtons</span></span>

<span data-ttu-id="221c8-202">Ocho controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-202">Eight button-family controls.</span></span><br/>

![imagen de la plantilla eightbuttons-lastthreesmall large sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![imagen de la plantilla eightbuttons-lastthreesmall medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![imagen de la plantilla eightbuttons-lastthreesmall small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="221c8-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="221c8-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="221c8-207">Ocho controles de familia de botones (presentación alternativa).</span><span class="sxs-lookup"><span data-stu-id="221c8-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="221c8-208">Todos los elementos de control declarados con esta plantilla deben estar contenidos en dos [**elementos ControlGroup:**](windowsribbon-element-controlgroup.md) uno para los cinco primeros elementos y otro para los tres últimos elementos.</span><span class="sxs-lookup"><span data-stu-id="221c8-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="221c8-209">En el ejemplo siguiente se muestra el marcado necesario para esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="221c8-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![imagen de la plantilla sizedefinition de ocho botones de gran tamaño.](images/overviews/sizedefinition-eightbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de ocho botones.](images/overviews/sizedefinition-eightbuttons-medium.png)

![imagen de la plantilla small sizedefinition de ocho botones.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="221c8-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-213">NineButtons</span></span>

<span data-ttu-id="221c8-214">Nueve controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-214">Nine button-family controls.</span></span>

![imagen de la plantilla de definición de tamaño grande de ninebuttons.](images/overviews/sizedefinition-ninebuttons-large.png)

![imagen de la plantilla ninebuttons medium sizedefinition.](images/overviews/sizedefinition-ninebuttons-medium.png)

![imagen de la plantilla small sizedefinition de ninebuttons.](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="221c8-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-218">TenButtons</span></span>

<span data-ttu-id="221c8-219">Diez controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-219">Ten button-family controls.</span></span>

![imagen de la plantilla de definición de tamaño grande de los botones de diez botones.](images/overviews/sizedefinition-tenbuttons-large.png)

![imagen de la plantilla tenbuttons medium sizedefinition.](images/overviews/sizedefinition-tenbuttons-medium.png)

![imagen de la plantilla small sizedefinition de tenbuttons.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="221c8-223">OnceButtons</span><span class="sxs-lookup"><span data-stu-id="221c8-223">ElevenButtons</span></span>

<span data-ttu-id="221c8-224">Once controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-224">Eleven button-family controls.</span></span>

![imagen de la plantilla de definición de tamaño grande de once botones.](images/overviews/sizedefinition-elevenbuttons-large.png)

![imagen de la plantilla de definición de tamaño medio de once botones.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![imagen de la plantilla small sizedefinition de once botones.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="221c8-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="221c8-228">OneFontControl</span></span>

<span data-ttu-id="221c8-229">Un [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="221c8-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="221c8-230">Solo se admiten tamaños de grupo grandes y medianos.</span><span class="sxs-lookup"><span data-stu-id="221c8-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="221c8-231">El marco de trabajo no admite la inclusión de [**un FontControl**](windowsribbon-element-fontcontrol.md) dentro de una definición de plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="221c8-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![imagen de una plantilla de definición de tamaño grande de onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-large.png)

![imagen de una plantilla de definición de tamaño medio de onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="221c8-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="221c8-234">OneInRibbonGallery</span></span>

<span data-ttu-id="221c8-235">Un [**control InRibbonGallery.**](windowsribbon-element-inribbongallery.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="221c8-236">Solo se admiten los tamaños de grupo grande y pequeño.</span><span class="sxs-lookup"><span data-stu-id="221c8-236">Only Large and Small group sizes are supported.</span></span>

![imagen de una plantilla de definición de tamaño grande de oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![imagen de una plantilla de definición de tamaño pequeño de oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="221c8-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="221c8-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="221c8-240">Un [**control InRibbonGallery**](windowsribbon-element-inribbongallery.md) y un control de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="221c8-241">Solo se admiten los tamaños de grupo grande y pequeño.</span><span class="sxs-lookup"><span data-stu-id="221c8-241">Only Large and Small group sizes are supported.</span></span>

![imagen de la plantilla inribbongalleryandbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![imagen de la plantilla inribbongalleryandbigbutton small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="221c8-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="221c8-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="221c8-245">Un [control de la Galería en la cinta de](windowsribbon-controls-inribbongallery.md) opciones y dos o tres controles de familia de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="221c8-246">La galería se contrae en la representación Popup en tamaños de grupo Mediano y Pequeño.</span><span class="sxs-lookup"><span data-stu-id="221c8-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![imagen de inribbongalleryandbuttons-galleryscalesfirst large sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![imagen de inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![imagen de inribbongalleryandbuttons-galleryscalesfirst small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="221c8-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="221c8-250">ButtonGroups</span></span>

<span data-ttu-id="221c8-251">Una disposición compleja de 32 controles de familia de botones (la mayoría de los cuales son opcionales).</span><span class="sxs-lookup"><span data-stu-id="221c8-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="221c8-252">Aparte del botón de tamaño completo opcional de la plantilla ButtonGroups grande, todos los elementos de control declarados con esta plantilla deben estar incluidos en [**los elementos ControlGroup.**](windowsribbon-element-controlgroup.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="221c8-253">En el ejemplo siguiente se muestra el marcado necesario para mostrar los 32 elementos de control (obligatorios y opcionales) con esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="221c8-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![imagen de la plantilla sizedefinition de grupos de botones de gran tamaño.](images/overviews/sizedefinition-buttongroups-large.png)

![imagen de la plantilla de definición de tamaño medio de los grupos de botones.](images/overviews/sizedefinition-buttongroups-medium.png)

![imagen de la plantilla small sizedefinition de grupos de botones.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="221c8-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="221c8-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="221c8-258">Dos controles de familia de entrada (el segundo es opcional) seguidos de una compleja disposición de 29 controles de familia de botones (la mayoría de los cuales son opcionales).</span><span class="sxs-lookup"><span data-stu-id="221c8-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="221c8-259">Solo se admiten tamaños de grupo grandes y medianos.</span><span class="sxs-lookup"><span data-stu-id="221c8-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="221c8-260">Todos los elementos de control declarados con esta plantilla deben estar incluidos en [**los elementos ControlGroup.**](windowsribbon-element-controlgroup.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="221c8-261">En el ejemplo siguiente se muestra el marcado necesario para mostrar todos los elementos de control (obligatorios y opcionales) con esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="221c8-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![imagen de la plantilla buttongroupsandinputs large sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![imagen de la plantilla buttongroupsandinputs medium sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="221c8-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="221c8-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="221c8-265">Dos controles de familia de botones (ambos opcionales) seguidos de dos o tres controles de botón o familia de entrada.</span><span class="sxs-lookup"><span data-stu-id="221c8-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="221c8-266">Solo se admiten tamaños de grupo grandes y medianos.</span><span class="sxs-lookup"><span data-stu-id="221c8-266">Only Large and Medium group sizes are supported.</span></span>

![imagen de la plantilla bigbuttonsandsmallbuttonsorinputs large sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![imagen de la plantilla bigbuttonsandsmallbuttonsorinputs medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="221c8-269">Ejemplo de SizeDefinition básico</span><span class="sxs-lookup"><span data-stu-id="221c8-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="221c8-270">En el ejemplo de código siguiente se proporciona una demostración básica de cómo declarar una [**plantilla SizeDefinition**](windowsribbon-element-sizedefinition.md) en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="221c8-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="221c8-271">*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) se usa para este ejemplo en particular, pero todas las plantillas de marco se especifican de forma similar.</span><span class="sxs-lookup"><span data-stu-id="221c8-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="221c8-272">Ejemplo de SizeDefinition complejo con directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="221c8-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="221c8-273">El comportamiento de con contraer las plantillas [**SizeDefinition**](windowsribbon-element-sizedefinition.md) se puede controlar mediante el uso de directivas de escalado en el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="221c8-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="221c8-274">El [**elemento ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifiesto de declaraciones [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) y [**Scale**](windowsribbon-element-scale.md) que especifican preferencias de diseño adaptable para uno o varios elementos [**Group**](windowsribbon-element-group.md) cuando se cambia el tamaño de la cinta.</span><span class="sxs-lookup"><span data-stu-id="221c8-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="221c8-275">Se recomienda encarecidamente especificar los detalles adecuados de la directiva de escalado de forma que la mayoría de los elementos [**Group,**](windowsribbon-element-group.md) si no todos, estén asociados a un elemento [**Scale**](windowsribbon-element-scale.md) donde el atributo *Size* sea igual a `Popup` .</span><span class="sxs-lookup"><span data-stu-id="221c8-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="221c8-276">Esto permite que el marco represente la cinta de opciones con el menor tamaño posible y admita la gama más amplia de dispositivos de visualización, antes de introducir automáticamente un mecanismo de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="221c8-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="221c8-277">En el ejemplo de código siguiente se muestra un [**manifiesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica una preferencia [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de los cuatro grupos de controles de una **pestaña** Inicio. Además, los [**elementos Scale**](windowsribbon-element-scale.md) se especifican para influir en el comportamiento de conserción, en orden descendente de tamaño, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="221c8-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="221c8-278">Plantillas personalizadas</span><span class="sxs-lookup"><span data-stu-id="221c8-278">Custom Templates</span></span>

<span data-ttu-id="221c8-279">Si los comportamientos de diseño predeterminados y las plantillas [**de SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidas no ofrecen la flexibilidad o compatibilidad para un escenario de diseño determinado, el marco de la cinta de opciones admite las plantillas personalizadas a través del elemento [**Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="221c8-280">Las plantillas personalizadas se pueden declarar de dos maneras: un método independiente mediante el elemento [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) para declarar plantillas reutilizables con nombre o un método en línea específico de [**Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="221c8-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="221c8-281">Plantilla independiente</span><span class="sxs-lookup"><span data-stu-id="221c8-281">Standalone Template</span></span>

<span data-ttu-id="221c8-282">En el ejemplo de código siguiente se muestra una plantilla personalizada básica y reutilizable.</span><span class="sxs-lookup"><span data-stu-id="221c8-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="221c8-283">Plantilla inserta</span><span class="sxs-lookup"><span data-stu-id="221c8-283">Inline Template</span></span>

<span data-ttu-id="221c8-284">En los ejemplos de código siguientes se muestra una plantilla personalizada en línea básica para un grupo de cuatro botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="221c8-285">En esta sección de código se muestran las declaraciones command para un grupo de botones.</span><span class="sxs-lookup"><span data-stu-id="221c8-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="221c8-286">Aquí también se especifican recursos de imagen grandes y pequeños.</span><span class="sxs-lookup"><span data-stu-id="221c8-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="221c8-287">En esta sección de código se muestra cómo definir plantillas [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) grandes, medianas y pequeñas para mostrar los cuatro botones en distintos tamaños y diseños.</span><span class="sxs-lookup"><span data-stu-id="221c8-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="221c8-288">La [**declaración ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de la pestaña define qué plantilla se usa para un grupo de controles en función del tamaño y el espacio de la cinta de opciones requeridos por la pestaña activa.</span><span class="sxs-lookup"><span data-stu-id="221c8-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="221c8-289">En las imágenes siguientes se muestra cómo se aplican las plantillas del ejemplo anterior a la interfaz de usuario de la cinta de opciones para dar cabida a una disminución del tamaño de la cinta.</span><span class="sxs-lookup"><span data-stu-id="221c8-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|  <span data-ttu-id="221c8-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="221c8-290">Type</span></span>  |      <span data-ttu-id="221c8-291">Imagen</span><span class="sxs-lookup"><span data-stu-id="221c8-291">Image</span></span>                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="221c8-292">grande</span><span class="sxs-lookup"><span data-stu-id="221c8-292">Large</span></span>  | ![imagen de una plantilla personalizada grande insertda.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="221c8-294">Media</span><span class="sxs-lookup"><span data-stu-id="221c8-294">Medium</span></span> | ![imagen de una plantilla personalizada mediana insertda.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="221c8-296">Pequeña</span><span class="sxs-lookup"><span data-stu-id="221c8-296">Small</span></span>  | ![imagen de una plantilla personalizada pequeña insertda.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="221c8-298">Popup</span><span class="sxs-lookup"><span data-stu-id="221c8-298">Popup</span></span>  | ![imagen de una plantilla personalizada emergente insertda.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="221c8-300">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="221c8-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="221c8-301">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="221c8-301">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="221c8-302">**Escala**</span><span class="sxs-lookup"><span data-stu-id="221c8-302">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="221c8-303">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="221c8-303">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





