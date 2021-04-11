---
title: Button (elemento, marco de cinta de Windows)
description: Representa un control de botón.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Elemento botón de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c037a598a4a853db3203162bcdbe6cd71afca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149306"
---
# <a name="button-element"></a><span data-ttu-id="4d6c9-104">Elemento Button</span><span class="sxs-lookup"><span data-stu-id="4d6c9-104">Button element</span></span>

<span data-ttu-id="4d6c9-105">Representa un control de [botón](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="4d6c9-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="4d6c9-106">Uso</span><span class="sxs-lookup"><span data-stu-id="4d6c9-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="4d6c9-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4d6c9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d6c9-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="4d6c9-108">Attribute</span></span></th>
<th><span data-ttu-id="4d6c9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d6c9-109">Type</span></span></th>
<th><span data-ttu-id="4d6c9-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d6c9-110">Required</span></span></th>
<th><span data-ttu-id="4d6c9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d6c9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d6c9-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="4d6c9-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="4d6c9-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="4d6c9-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="4d6c9-114">No</span><span class="sxs-lookup"><span data-stu-id="4d6c9-114">No</span></span><br/></td>
<td><span data-ttu-id="4d6c9-115">Este atributo solo es válido cuando el elemento de <strong>botón</strong> es un elemento secundario de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="4d6c9-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="4d6c9-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="4d6c9-117">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="4d6c9-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="4d6c9-118">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-118">Default.</span></span> <br/> </dd> <span data-ttu-id="4d6c9-119"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="4d6c9-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d6c9-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="4d6c9-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="4d6c9-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="4d6c9-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="4d6c9-122">No</span><span class="sxs-lookup"><span data-stu-id="4d6c9-122">No</span></span><br/></td>
<td><span data-ttu-id="4d6c9-123">Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="4d6c9-124">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="4d6c9-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4d6c9-125">Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="4d6c9-126">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="4d6c9-127">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d6c9-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="4d6c9-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="4d6c9-129">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="4d6c9-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="4d6c9-130">No</span><span class="sxs-lookup"><span data-stu-id="4d6c9-130">No</span></span><br/></td>
<td><span data-ttu-id="4d6c9-131">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="4d6c9-132">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="4d6c9-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4d6c9-133">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="4d6c9-134">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="4d6c9-135">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="4d6c9-136">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d6c9-136">Child elements</span></span>

<span data-ttu-id="4d6c9-137">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4d6c9-138">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4d6c9-138">Parent elements</span></span>



| <span data-ttu-id="4d6c9-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="4d6c9-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d6c9-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="4d6c9-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="4d6c9-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="4d6c9-143">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="4d6c9-144">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="4d6c9-145">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="4d6c9-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="4d6c9-147">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="4d6c9-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="4d6c9-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d6c9-149">Remarks</span></span>

<span data-ttu-id="4d6c9-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-150">Optional.</span></span>

<span data-ttu-id="4d6c9-151">Puede aparecer como máximo una vez por cada elemento [**splitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4d6c9-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="4d6c9-152">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="4d6c9-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="4d6c9-153">El **botón** admite [modos de aplicación](ribbon-applicationmodes.md) cuando se hospeda en la columna izquierda del menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="4d6c9-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d6c9-154">Examples</span></span>

<span data-ttu-id="4d6c9-155">En el ejemplo siguiente se muestra el marcado básico para el **botón**.</span><span class="sxs-lookup"><span data-stu-id="4d6c9-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="4d6c9-156">En esta sección de código se muestran las declaraciones de comando de **botón** , con un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario del elemento de **botón** .</span><span class="sxs-lookup"><span data-stu-id="4d6c9-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


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



<span data-ttu-id="4d6c9-157">En esta sección de código se muestran las declaraciones de control de **botón** .</span><span class="sxs-lookup"><span data-stu-id="4d6c9-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="4d6c9-158">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d6c9-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="4d6c9-159">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d6c9-159">Minimum supported system</span></span><br/> | <span data-ttu-id="4d6c9-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d6c9-160">Windows 7</span></span> |
| <span data-ttu-id="4d6c9-161">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4d6c9-161">Can be empty</span></span>                        | <span data-ttu-id="4d6c9-162">Sí</span><span class="sxs-lookup"><span data-stu-id="4d6c9-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="4d6c9-163">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d6c9-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d6c9-164">Button (control)</span><span class="sxs-lookup"><span data-stu-id="4d6c9-164">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="4d6c9-165">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="4d6c9-165">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

