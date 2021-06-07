---
title: Drop-Down Selector de colores
description: El marco de la cinta de opciones de Windows proporciona un control Drop-Down Selector de colores que expone una variedad de configuraciones de color a través de un botón de división y un selector de colores desplegable personalizable.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443666"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="70b61-103">Drop-Down Selector de colores</span><span class="sxs-lookup"><span data-stu-id="70b61-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="70b61-104">El marco de la cinta de opciones de Windows proporciona un control Drop-Down Selector de colores que expone una variedad de configuraciones de color a través de un botón de división y un selector de colores desplegable personalizable.</span><span class="sxs-lookup"><span data-stu-id="70b61-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="70b61-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="70b61-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="70b61-106">marcado</span><span class="sxs-lookup"><span data-stu-id="70b61-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="70b61-107">Código</span><span class="sxs-lookup"><span data-stu-id="70b61-107">Code</span></span>](#code)
    -   [<span data-ttu-id="70b61-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70b61-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="70b61-109">Controladores de comandos</span><span class="sxs-lookup"><span data-stu-id="70b61-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="70b61-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70b61-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="70b61-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="70b61-111">Introduction</span></span>

<span data-ttu-id="70b61-112">Mediante la emulación de la apariencia y la funcionalidad del selector de colores Microsoft Office, el marco de la cinta de opciones puede beneficiarse de la coherencia y familiaridad de una amplia gama de aplicaciones y contribuir a ello.</span><span class="sxs-lookup"><span data-stu-id="70b61-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="70b61-113">marcado</span><span class="sxs-lookup"><span data-stu-id="70b61-113">Markup</span></span>

<span data-ttu-id="70b61-114">Al igual que todos los controles de la cinta de opciones, Drop-Down Selector de colores se implementa y personaliza fácilmente a través del marcado.</span><span class="sxs-lookup"><span data-stu-id="70b61-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="70b61-115">El marco proporciona una serie de atributos de elemento para que el Drop-Down Selector de colores exponga varios niveles de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="70b61-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="70b61-116">En la tabla siguiente se enumeran los Drop-Down Selector de colores atributos.</span><span class="sxs-lookup"><span data-stu-id="70b61-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70b61-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="70b61-117">Attribute</span></span></th>
<th><span data-ttu-id="70b61-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="70b61-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70b61-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="70b61-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="70b61-120">Plantillas de diseño que especifican el tipo de Drop-Down Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="70b61-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="70b61-121">Hay tres plantillas, cada una de las cuales especifica un diseño de control y valores predeterminados para los atributos asociados y las claves de propiedad.</span><span class="sxs-lookup"><span data-stu-id="70b61-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-122">ChipSize</span><span class="sxs-lookup"><span data-stu-id="70b61-122">ChipSize</span></span></td>
<td><span data-ttu-id="70b61-123">Tamaño de cada chip de color (o muestra).</span><span class="sxs-lookup"><span data-stu-id="70b61-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-124">Columnas</span><span class="sxs-lookup"><span data-stu-id="70b61-124">Columns</span></span></td>
<td><span data-ttu-id="70b61-125">Número de columnas de chip de color (o muestra).</span><span class="sxs-lookup"><span data-stu-id="70b61-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="70b61-126">CommandName</span></span></td>
<td><span data-ttu-id="70b61-127">Nombre de la declaración Command asociada.</span><span class="sxs-lookup"><span data-stu-id="70b61-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="70b61-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="70b61-129">Muestra (u oculta) el <strong>botón</strong> Automático.</span><span class="sxs-lookup"><span data-stu-id="70b61-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="70b61-130">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="70b61-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="70b61-132">Muestra (u oculta) el <strong>botón Sin</strong> color.</span><span class="sxs-lookup"><span data-stu-id="70b61-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="70b61-133">Válido para todos los <em>valores de ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="70b61-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="70b61-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="70b61-135">Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> recientes.</span><span class="sxs-lookup"><span data-stu-id="70b61-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="70b61-136">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="70b61-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="70b61-138">Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> estándar.</span><span class="sxs-lookup"><span data-stu-id="70b61-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="70b61-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="70b61-140">Número de filas de chip de color (o muestra) en el área <strong>Colores del</strong> tema.</span><span class="sxs-lookup"><span data-stu-id="70b61-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="70b61-141">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70b61-142">En las siguientes capturas de pantalla se muestran los Drop-Down Selector de colores diseños predeterminados para las tres plantillas de color.</span><span class="sxs-lookup"><span data-stu-id="70b61-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b61-143">`ThemeColors`: \[ captura de pantalla de nueva línea del elemento \] ![ dropdowncolorpicker con el atributo colortemplate establecido en "themecolors". ](images/markup/colortemplate.themedcolors.1.png) \[ Newline\]</span><span class="sxs-lookup"><span data-stu-id="70b61-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="70b61-144">`standardcolors`: \[ captura de pantalla de nueva línea del elemento \] ![ dropdowncolorpicker con el atributo colortemplate establecido en "standardcolors". ](images/markup/colortemplate.standardcolors.3.png) \[ Newline\]</span><span class="sxs-lookup"><span data-stu-id="70b61-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="70b61-145">`highlightcolors`: \[ captura de pantalla de nueva línea del elemento \] ![ dropdowncolorpicker con el atributo colortemplate establecido en "highlightcolors".](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="70b61-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="70b61-146">El marcado básico necesario para cada tipo Drop-Down Selector de colores se muestra en los ejemplos siguientes:</span><span class="sxs-lookup"><span data-stu-id="70b61-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="70b61-147">El Drop-Down Selector de colores es un control [Button](windowsribbon-controls-button.md) válido en una [**plantilla SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="70b61-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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





## <a name="code"></a><span data-ttu-id="70b61-148">Código</span><span class="sxs-lookup"><span data-stu-id="70b61-148">Code</span></span>

<span data-ttu-id="70b61-149">Como control especializado que admite la personalización, cualquier implementación del Drop-Down Selector de colores que aproveche estas funcionalidades requiere código de aplicación especializado para administrar las propiedades y controlar los comandos emitidos por el control.</span><span class="sxs-lookup"><span data-stu-id="70b61-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="70b61-150">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70b61-150">Properties</span></span>

<span data-ttu-id="70b61-151">El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el Drop-Down Selector de colores control .</span><span class="sxs-lookup"><span data-stu-id="70b61-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="70b61-152">Normalmente, una propiedad Drop-Down Selector de colores se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)</span><span class="sxs-lookup"><span data-stu-id="70b61-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="70b61-153">El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.</span><span class="sxs-lookup"><span data-stu-id="70b61-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="70b61-154">El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco requiere la propiedad .</span><span class="sxs-lookup"><span data-stu-id="70b61-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="70b61-155">Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="70b61-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="70b61-156">En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)</span><span class="sxs-lookup"><span data-stu-id="70b61-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="70b61-157">En la tabla siguiente se enumeran las claves de propiedad asociadas al control Drop-Down Selector de colores control .</span><span class="sxs-lookup"><span data-stu-id="70b61-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70b61-158">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="70b61-158">Property Key</span></span></th>
<th><span data-ttu-id="70b61-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="70b61-159">Description</span></span></th>
<th><span data-ttu-id="70b61-160">Notas</span><span class="sxs-lookup"><span data-stu-id="70b61-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70b61-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="70b61-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="70b61-162">Define la etiqueta del <strong>botón</strong> Color automático.</span><span class="sxs-lookup"><span data-stu-id="70b61-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="70b61-163">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="70b61-164">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="70b61-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="70b61-166">Define el valor de color seleccionado como <a href="/windows/win32/gdi/colorref">COLORREF.</a></span><span class="sxs-lookup"><span data-stu-id="70b61-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="70b61-167">Solo es válido <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tiene un valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="70b61-168">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="70b61-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="70b61-170">Define el tipo de color seleccionado.</span><span class="sxs-lookup"><span data-stu-id="70b61-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="70b61-171">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="70b61-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="70b61-173">Define la capacidad de un control para responder a la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="70b61-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="70b61-174">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="70b61-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="70b61-176">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="70b61-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="70b61-178">Define la cadena de caracteres de una etiqueta de control.</span><span class="sxs-lookup"><span data-stu-id="70b61-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="70b61-179">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="70b61-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="70b61-181">Define la imagen de contraste alto grande que se mostrará para un control.</span><span class="sxs-lookup"><span data-stu-id="70b61-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="70b61-182">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="70b61-183">Para obtener más información sobre los formatos de imagen, vea Especificar recursos de imagen de cinta de <a href="windowsribbon-imageformats.md">opciones.</a></span><span class="sxs-lookup"><span data-stu-id="70b61-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="70b61-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="70b61-185">Define la imagen grande que se mostrará para un control .</span><span class="sxs-lookup"><span data-stu-id="70b61-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="70b61-186">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="70b61-187">Para obtener más información sobre los formatos de imagen, vea Especificar recursos de imagen de cinta de <a href="windowsribbon-imageformats.md">opciones.</a></span><span class="sxs-lookup"><span data-stu-id="70b61-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="70b61-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="70b61-189">Define la etiqueta del botón <strong>Más</strong> colores....</span><span class="sxs-lookup"><span data-stu-id="70b61-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="70b61-190">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="70b61-191">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="70b61-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="70b61-193">Define la etiqueta del botón <strong>Sin</strong> color.</span><span class="sxs-lookup"><span data-stu-id="70b61-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="70b61-194">Válido para todos los <em>valores de ColorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="70b61-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="70b61-195">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="70b61-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="70b61-197">Define la etiqueta de la <strong>categoría Colores</strong> recientes.</span><span class="sxs-lookup"><span data-stu-id="70b61-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="70b61-198">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="70b61-199">Esta es la única plantilla que contiene categorías etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="70b61-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="70b61-200">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="70b61-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="70b61-202">Define la imagen pequeña de contraste alto que se mostrará para un control.</span><span class="sxs-lookup"><span data-stu-id="70b61-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="70b61-203">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="70b61-204">Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">Especificar recursos de imagen de la cinta de opciones.</a></span><span class="sxs-lookup"><span data-stu-id="70b61-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="70b61-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="70b61-206">Define la imagen pequeña que se mostrará para un control .</span><span class="sxs-lookup"><span data-stu-id="70b61-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="70b61-207">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="70b61-208">Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">Especificar recursos de imagen de la cinta de opciones.</a></span><span class="sxs-lookup"><span data-stu-id="70b61-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="70b61-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="70b61-210">Define una matriz <a href="/windows/win32/gdi/colorref">de valores COLORREF</a> para las muestras de un Drop-Down Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="70b61-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="70b61-211">Cada Drop-Down Selector de colores <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="70b61-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="70b61-212">Se muestran los valores <a href="/windows/win32/gdi/colorref">COLORREF</a> de <em>la columna StandardColorGridRows</em> x <em>inicial</em> de la matriz.</span><span class="sxs-lookup"><span data-stu-id="70b61-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="70b61-213">Si la matriz define menos colores que el número de muestras declaradas en el marcado, se muestran espacios vacíos para los chips <code>StandardColors</code> que faltan.</span><span class="sxs-lookup"><span data-stu-id="70b61-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="70b61-214">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="70b61-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="70b61-216">Define la etiqueta para la <strong>categoría Colores</strong> estándar.</span><span class="sxs-lookup"><span data-stu-id="70b61-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="70b61-217">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="70b61-218">Esta es la única plantilla que contiene categorías etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="70b61-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="70b61-219">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="70b61-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="70b61-221">Define una matriz de cadenas de información sobre herramientas de la muestra de color para la <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="70b61-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="70b61-222">Cada Drop-Down Selector de colores <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="70b61-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="70b61-223">Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en <code>StandardColors</code> la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="70b61-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="70b61-224">Si se proporcionan menos etiquetas que el número de muestras de la cuadrícula, se proporciona un valor predeterminado para las muestras <code>StandardColors</code> que permanecen.</span><span class="sxs-lookup"><span data-stu-id="70b61-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="70b61-225">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="70b61-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="70b61-227">Define una matriz <a href="/windows/win32/gdi/colorref">de valores COLORREF</a> para las muestras de un Drop-Down Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="70b61-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="70b61-228">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="70b61-229">Se muestran los valores <a href="/windows/win32/gdi/colorref">COLORREF</a> de <em>la columna ThemeColorGridRows</em> <em>x</em> inicial de la matriz.</span><span class="sxs-lookup"><span data-stu-id="70b61-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="70b61-230">Si la matriz define menos colores que el número de muestras declaradas en el marcado, se muestran espacios vacíos para los chips <code>ThemeColors</code> que faltan.</span><span class="sxs-lookup"><span data-stu-id="70b61-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="70b61-231">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="70b61-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="70b61-233">Define la matriz de cadenas de información sobre herramientas de la muestra de color para la <code>ThemeColors</code> cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="70b61-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="70b61-234">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="70b61-235">Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en <code>ThemeColors</code> la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="70b61-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="70b61-236">Si se proporcionan menos etiquetas que el número de muestras de la cuadrícula, se proporciona un valor predeterminado para las muestras <code>ThemeColors</code> que permanecen.</span><span class="sxs-lookup"><span data-stu-id="70b61-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="70b61-237">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="70b61-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="70b61-239">Define la etiqueta de la categoría <strong>Colores del</strong> tema.</span><span class="sxs-lookup"><span data-stu-id="70b61-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="70b61-240">Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="70b61-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="70b61-241">Esta es la única plantilla que contiene categorías etiquetadas.</span><span class="sxs-lookup"><span data-stu-id="70b61-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="70b61-242">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70b61-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="70b61-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="70b61-244">Define la cadena de caracteres para una descripción de información sobre herramientas asociada a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">un UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="70b61-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="70b61-245">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70b61-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="70b61-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="70b61-247">Define la cadena de caracteres para una información sobre herramientas de comandos.</span><span class="sxs-lookup"><span data-stu-id="70b61-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="70b61-248">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="70b61-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="70b61-249">Controladores de comandos</span><span class="sxs-lookup"><span data-stu-id="70b61-249">Command handlers</span></span>

<span data-ttu-id="70b61-250">El [**método IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) se usa para personalizar un Drop-Down Selector de colores a través de las claves de propiedad enumeradas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="70b61-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="70b61-251">En el ejemplo siguiente se muestra cómo establecer las muestras de color de un Drop-Down Selector de colores, en función de una preferencia de estilo personalizado o una cuadrícula de muestra personalizada que se declara en el marcado.</span><span class="sxs-lookup"><span data-stu-id="70b61-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


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



<span data-ttu-id="70b61-252">En el ejemplo siguiente se muestra una implementación del método [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expone los colores Drop-Down Selector de colores muestra a la aplicación Ribbon.</span><span class="sxs-lookup"><span data-stu-id="70b61-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="70b61-253">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70b61-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70b61-254">Biblioteca de controles del marco de opciones de Windows</span><span class="sxs-lookup"><span data-stu-id="70b61-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="70b61-255">**Elemento de marcado DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="70b61-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="70b61-256">Selector de colores propiedades</span><span class="sxs-lookup"><span data-stu-id="70b61-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="70b61-257">Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado</span><span class="sxs-lookup"><span data-stu-id="70b61-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="70b61-258">Ejemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="70b61-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

