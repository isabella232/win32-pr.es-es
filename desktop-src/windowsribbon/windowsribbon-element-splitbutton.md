---
title: Elemento SplitButton
description: Representa un control Split Button estándar.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Elemento SplitButton de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf03d85dd0402548d02f107dafb209b68c13bb72
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444406"
---
# <a name="splitbutton-element"></a><span data-ttu-id="89414-104">Elemento SplitButton</span><span class="sxs-lookup"><span data-stu-id="89414-104">SplitButton element</span></span>

<span data-ttu-id="89414-105">Representa un control [Split Button](windowsribbon-controls-splitbutton.md) estándar.</span><span class="sxs-lookup"><span data-stu-id="89414-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="89414-106">Uso</span><span class="sxs-lookup"><span data-stu-id="89414-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="89414-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="89414-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89414-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="89414-108">Attribute</span></span></th>
<th><span data-ttu-id="89414-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="89414-109">Type</span></span></th>
<th><span data-ttu-id="89414-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="89414-110">Required</span></span></th>
<th><span data-ttu-id="89414-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="89414-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89414-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="89414-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="89414-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="89414-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="89414-114">No</span><span class="sxs-lookup"><span data-stu-id="89414-114">No</span></span><br/></td>
<td><span data-ttu-id="89414-115">Solo es válido <a href="windowsribbon-element-menugroup.md"><strong>si MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="89414-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="89414-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="89414-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89414-117">Cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="89414-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="89414-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="89414-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="89414-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="89414-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89414-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="89414-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="89414-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="89414-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="89414-122">No</span><span class="sxs-lookup"><span data-stu-id="89414-122">No</span></span><br/></td>
<td><span data-ttu-id="89414-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="89414-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="89414-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="89414-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89414-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="89414-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="89414-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="89414-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="89414-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="89414-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="89414-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89414-128">Child elements</span></span>



| <span data-ttu-id="89414-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="89414-129">Element</span></span>                                                                                   | <span data-ttu-id="89414-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="89414-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="89414-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="89414-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="89414-132">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89414-133">**Casilla**</span><span class="sxs-lookup"><span data-stu-id="89414-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="89414-134">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89414-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="89414-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="89414-136">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89414-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="89414-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="89414-138">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89414-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="89414-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="89414-140">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="89414-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="89414-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="89414-142">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89414-143">**SplitButton.ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="89414-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="89414-144">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="89414-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="89414-145">**SplitButton.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="89414-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="89414-146">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="89414-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="89414-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="89414-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="89414-148">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89414-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="89414-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="89414-150">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="89414-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="89414-151">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="89414-151">Parent elements</span></span>



| <span data-ttu-id="89414-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="89414-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="89414-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="89414-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="89414-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="89414-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="89414-155">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="89414-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="89414-156">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="89414-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="89414-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="89414-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="89414-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="89414-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="89414-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89414-159">Remarks</span></span>

<span data-ttu-id="89414-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="89414-160">Optional.</span></span>

<span data-ttu-id="89414-161">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="89414-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="89414-162">**SplitButton** admite [modos de](ribbon-applicationmodes.md) aplicación cuando se hospeda en la columna izquierda del menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89414-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="89414-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) y [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) no son elementos secundarios válidos de [**DropDownButton**](windowsribbon-element-dropdownbutton.md) cuando **DropDownButton** es un descendiente de [**ApplicationMenu.**](windowsribbon-element-applicationmenu.md)</span><span class="sxs-lookup"><span data-stu-id="89414-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="89414-164">[**SplitButton.MenuGroups debe**](windowsribbon-element-splitbutton-menugroups.md) producirse una vez si lo siguiente no está presente como elementos secundarios de **SplitButton**:</span><span class="sxs-lookup"><span data-stu-id="89414-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="89414-165">**Button**</span><span class="sxs-lookup"><span data-stu-id="89414-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="89414-166">**Casilla**</span><span class="sxs-lookup"><span data-stu-id="89414-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="89414-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="89414-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="89414-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="89414-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="89414-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="89414-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="89414-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="89414-170">**SplitButton**</span></span>
-   [<span data-ttu-id="89414-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="89414-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="89414-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="89414-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="89414-173">Estos controles se tratan como elementos secundarios de un único [**elemento SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="89414-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="89414-174">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="89414-174">Examples</span></span>

<span data-ttu-id="89414-175">En el ejemplo siguiente se muestra el marcado básico para el [botón Dividir](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="89414-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="89414-176">En esta sección de código se muestran las declaraciones del comando **SplitButton,** con un [**grupo**](windowsribbon-element-group.md) asociado que funciona como contenedor primario para el **elemento SplitButton.**</span><span class="sxs-lookup"><span data-stu-id="89414-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="89414-177">En esta sección de código se muestran las declaraciones de control **SplitButton.**</span><span class="sxs-lookup"><span data-stu-id="89414-177">This section of code shows the **SplitButton** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="89414-178">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="89414-178">Element information</span></span>

- <span data-ttu-id="89414-179">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="89414-179">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="89414-180">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="89414-180">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="89414-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="89414-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89414-182">Split Button (Control)</span><span class="sxs-lookup"><span data-stu-id="89414-182">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="89414-183">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="89414-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

