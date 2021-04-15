---
title: Selector de colores de Drop-Down
description: El marco de la cinta de opciones de Windows proporciona un control de selector de colores Drop-Down especializado que expone una variedad de valores de color a través de un botón de expansión y del selector de colores desplegables personalizables.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104421514"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="dc979-103">Selector de colores de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="dc979-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="dc979-104">El marco de la cinta de opciones de Windows proporciona un control de selector de colores Drop-Down especializado que expone una variedad de valores de color a través de un botón de expansión y del selector de colores desplegables personalizables.</span><span class="sxs-lookup"><span data-stu-id="dc979-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="dc979-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="dc979-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="dc979-106">marcado</span><span class="sxs-lookup"><span data-stu-id="dc979-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="dc979-107">Código</span><span class="sxs-lookup"><span data-stu-id="dc979-107">Code</span></span>](#code)
    -   [<span data-ttu-id="dc979-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc979-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="dc979-109">Controladores de comandos</span><span class="sxs-lookup"><span data-stu-id="dc979-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="dc979-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc979-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="dc979-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="dc979-111">Introduction</span></span>

<span data-ttu-id="dc979-112">Mediante la emulación de la apariencia y la funcionalidad de la Microsoft Office selector de color, el marco de la cinta de opciones puede beneficiarse de la coherencia y la familiaridad en una amplia gama de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dc979-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="dc979-113">marcado</span><span class="sxs-lookup"><span data-stu-id="dc979-113">Markup</span></span>

<span data-ttu-id="dc979-114">Al igual que todos los controles de la cinta de opciones, el selector de colores Drop-Down se implementa y personaliza fácilmente mediante marcado.</span><span class="sxs-lookup"><span data-stu-id="dc979-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="dc979-115">El marco de trabajo proporciona una serie de atributos de elemento para que el selector de colores de Drop-Down exponga varios niveles de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="dc979-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="dc979-116">En la tabla siguiente se enumeran los atributos del selector de colores de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="dc979-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc979-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="dc979-117">Attribute</span></span></th>
<th><span data-ttu-id="dc979-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc979-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc979-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="dc979-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="dc979-120">Plantillas de diseño que especifican el tipo de Drop-Down selector de colores.</span><span class="sxs-lookup"><span data-stu-id="dc979-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="dc979-121">Hay tres plantillas, cada una de las cuales especifica un diseño de control y valores predeterminados para los atributos y las claves de propiedad asociados.</span><span class="sxs-lookup"><span data-stu-id="dc979-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-122">Chip</span><span class="sxs-lookup"><span data-stu-id="dc979-122">ChipSize</span></span></td>
<td><span data-ttu-id="dc979-123">Tamaño de cada chip de color (o muestra).</span><span class="sxs-lookup"><span data-stu-id="dc979-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-124">Columnas</span><span class="sxs-lookup"><span data-stu-id="dc979-124">Columns</span></span></td>
<td><span data-ttu-id="dc979-125">El número de columnas de chip de color (o muestra).</span><span class="sxs-lookup"><span data-stu-id="dc979-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="dc979-126">CommandName</span></span></td>
<td><span data-ttu-id="dc979-127">Nombre de la declaración de comando asociada.</span><span class="sxs-lookup"><span data-stu-id="dc979-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="dc979-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="dc979-129">Muestra u oculta el botón <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="dc979-130">Válido solo cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="dc979-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="dc979-132">Muestra u oculta el botón <strong>sin color</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="dc979-133">Válido para todos los valores de <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="dc979-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="dc979-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="dc979-135">El número de filas del chip de color (o muestra) en el área de <strong>colores recientes</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="dc979-136">Válido solo cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="dc979-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="dc979-138">El número de filas del chip de color (o muestra) en el área <strong>colores estándar</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="dc979-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="dc979-140">El número de filas del chip de color (o muestra) en el área <strong>colores del tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="dc979-141">Válido solo cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dc979-142">En las siguientes capturas de pantalla se muestran los diseños predeterminados del selector de colores Drop-Down para las tres plantillas de color.</span><span class="sxs-lookup"><span data-stu-id="dc979-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc979-143">`ThemeColors`: \[ \] ![ captura de pantalla de nueva línea del elemento dropdowncolorpicker con el atributo colortemplate establecido en ' ThemeColors '. ](images/markup/colortemplate.themedcolors.1.png) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="dc979-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="dc979-144">`standardcolors`: \[ \] ![ captura de pantalla de nueva línea del elemento dropdowncolorpicker con el atributo colortemplate establecido en ' standardcolors '. ](images/markup/colortemplate.standardcolors.3.png) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="dc979-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="dc979-145">`highlightcolors`: \[ \] ![ captura de pantalla de nueva línea del elemento dropdowncolorpicker con el atributo colortemplate establecido en ' highlightcolors '.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="dc979-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="dc979-146">El marcado básico necesario para cada tipo de selector de color de Drop-Down se muestra en los ejemplos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc979-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="dc979-147">El selector de colores Drop-Down es un control de [botón](windowsribbon-controls-button.md) válido en una plantilla [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="dc979-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a><span data-ttu-id="dc979-148">Código</span><span class="sxs-lookup"><span data-stu-id="dc979-148">Code</span></span>

<span data-ttu-id="dc979-149">Como control especializado que admite la personalización, cualquier implementación de la Drop-Down selector de colores que aprovecha estas funcionalidades requiere código de aplicación especializado para administrar propiedades y controlar los comandos emitidos por el control.</span><span class="sxs-lookup"><span data-stu-id="dc979-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="dc979-150">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc979-150">Properties</span></span>

<span data-ttu-id="dc979-151">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control selector de color Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="dc979-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="dc979-152">Normalmente, una propiedad del selector de colores Drop-Down se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="dc979-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="dc979-153">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="dc979-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="dc979-154">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="dc979-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="dc979-155">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="dc979-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="dc979-156">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="dc979-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="dc979-157">En la tabla siguiente se enumeran las claves de propiedades que están asociadas con el control selector de color Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="dc979-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc979-158">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="dc979-158">Property Key</span></span></th>
<th><span data-ttu-id="dc979-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc979-159">Description</span></span></th>
<th><span data-ttu-id="dc979-160">Notas</span><span class="sxs-lookup"><span data-stu-id="dc979-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc979-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="dc979-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="dc979-162">Define la etiqueta del botón de color <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="dc979-163">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="dc979-164">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="dc979-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="dc979-166">Define el valor de color seleccionado como <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="dc979-167">Solo es válido cuando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tiene un valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="dc979-168">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="dc979-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="dc979-170">Define el tipo de color seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dc979-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="dc979-171">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="dc979-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="dc979-173">Define la capacidad de un control para responder a la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="dc979-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="dc979-174">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="dc979-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="dc979-176">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="dc979-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="dc979-178">Define la cadena de caracteres para una etiqueta de control.</span><span class="sxs-lookup"><span data-stu-id="dc979-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="dc979-179">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="dc979-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="dc979-181">Define la imagen grande de contraste alto que se va a mostrar para un control.</span><span class="sxs-lookup"><span data-stu-id="dc979-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="dc979-182">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="dc979-183">Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.</span><span class="sxs-lookup"><span data-stu-id="dc979-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="dc979-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="dc979-185">Define la imagen grande que se va a mostrar para un control.</span><span class="sxs-lookup"><span data-stu-id="dc979-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="dc979-186">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="dc979-187">Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.</span><span class="sxs-lookup"><span data-stu-id="dc979-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="dc979-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="dc979-189">Define la etiqueta para el botón <strong>más colores...</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="dc979-190">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="dc979-191">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="dc979-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="dc979-193">Define la etiqueta para el botón <strong>sin color</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="dc979-194">Válido para todos los valores de <em>ColorTemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="dc979-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="dc979-195">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="dc979-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="dc979-197">Define la etiqueta de la categoría de <strong>colores recientes</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="dc979-198">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="dc979-199">Esta es la única plantilla que contiene categorías etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="dc979-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="dc979-200">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="dc979-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="dc979-202">Define la pequeña imagen de contraste alto que se va a mostrar para un control.</span><span class="sxs-lookup"><span data-stu-id="dc979-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="dc979-203">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="dc979-204">Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.</span><span class="sxs-lookup"><span data-stu-id="dc979-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="dc979-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="dc979-206">Define la imagen pequeña que se va a mostrar para un control.</span><span class="sxs-lookup"><span data-stu-id="dc979-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="dc979-207">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="dc979-208">Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.</span><span class="sxs-lookup"><span data-stu-id="dc979-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="dc979-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="dc979-210">Define una matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para las muestras de un selector de color Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="dc979-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="dc979-211">Cada Drop-Down selector de color <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="dc979-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc979-212">Se muestran los valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> de las <em>columnas</em> <em>StandardColorGridRows</em> x iniciales de la matriz.</span><span class="sxs-lookup"><span data-stu-id="dc979-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="dc979-213">Si la matriz define menos colores que el número de <code>StandardColors</code> muestras declaradas en el marcado, se muestran espacios vacíos para los chips que faltan.</span><span class="sxs-lookup"><span data-stu-id="dc979-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="dc979-214">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="dc979-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="dc979-216">Define la etiqueta de la categoría de <strong>colores estándar</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="dc979-217">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="dc979-218">Esta es la única plantilla que contiene categorías etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="dc979-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="dc979-219">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="dc979-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="dc979-221">Define una matriz de cadenas de información sobre herramientas de muestrario de colores para la <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="dc979-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="dc979-222">Cada Drop-Down selector de color <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="dc979-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc979-223">Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en la <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="dc979-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="dc979-224">Si se proporcionan menos etiquetas que el número de muestras de la <code>StandardColors</code> cuadrícula, se proporciona un valor predeterminado para las muestras de remainining.</span><span class="sxs-lookup"><span data-stu-id="dc979-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="dc979-225">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="dc979-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="dc979-227">Define una matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para las muestras de un selector de color Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="dc979-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="dc979-228">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc979-229">Se muestran los valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> de las <em>columnas</em> <em>ThemeColorGridRows</em> x iniciales de la matriz.</span><span class="sxs-lookup"><span data-stu-id="dc979-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="dc979-230">Si la matriz define menos colores que el número de <code>ThemeColors</code> muestras declaradas en el marcado, se muestran espacios vacíos para los chips que faltan.</span><span class="sxs-lookup"><span data-stu-id="dc979-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="dc979-231">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="dc979-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="dc979-233">Define la matriz de cadenas de la información sobre herramientas del muestrario de colores para la <code>ThemeColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="dc979-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="dc979-234">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc979-235">Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en la <code>ThemeColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="dc979-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="dc979-236">Si se proporcionan menos etiquetas que el número de muestras de la <code>ThemeColors</code> cuadrícula, se proporciona un valor predeterminado para las muestras de remainining.</span><span class="sxs-lookup"><span data-stu-id="dc979-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="dc979-237">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="dc979-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="dc979-239">Define la etiqueta de la categoría de <strong>colores del tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc979-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="dc979-240">Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="dc979-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="dc979-241">Esta es la única plantilla que contiene categorías etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="dc979-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="dc979-242">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc979-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="dc979-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="dc979-244">Define la cadena de caracteres para una descripción de la información sobre herramientas asociada a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="dc979-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="dc979-245">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc979-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="dc979-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="dc979-247">Define la cadena de caracteres para la información sobre herramientas de un comando.</span><span class="sxs-lookup"><span data-stu-id="dc979-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="dc979-248">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="dc979-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="dc979-249">Controladores de comandos</span><span class="sxs-lookup"><span data-stu-id="dc979-249">Command handlers</span></span>

<span data-ttu-id="dc979-250">El método [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) se usa para personalizar un selector de colores Drop-Down a través de las claves de propiedad indicadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="dc979-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="dc979-251">En el ejemplo siguiente se muestra cómo establecer las muestras de color de un selector de colores Drop-Down, en función de una preferencia de estilo personalizado o una cuadrícula de muestra personalizada que se declara en el marcado.</span><span class="sxs-lookup"><span data-stu-id="dc979-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



<span data-ttu-id="dc979-252">En el ejemplo siguiente se muestra una implementación del método [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expone el Drop-Down colores del muestrario del selector de colores a la aplicación de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="dc979-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dc979-253">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc979-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc979-254">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="dc979-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="dc979-255">**Elemento de marcado DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="dc979-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="dc979-256">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="dc979-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="dc979-257">Personalización de una cinta a través de definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="dc979-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="dc979-258">Ejemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="dc979-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

