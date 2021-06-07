---
title: Elemento Button (Marco de la cinta de opciones de Windows)
description: Representa un control Button.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Botón, elemento De la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40236b60a9fe9c72dd35d67fcf7c98bc188938af
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443576"
---
# <a name="button-element"></a><span data-ttu-id="a433c-104">Elemento Button</span><span class="sxs-lookup"><span data-stu-id="a433c-104">Button element</span></span>

<span data-ttu-id="a433c-105">Representa un control [Button.](windowsribbon-controls-button.md)</span><span class="sxs-lookup"><span data-stu-id="a433c-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="a433c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a433c-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="a433c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a433c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a433c-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a433c-108">Attribute</span></span></th>
<th><span data-ttu-id="a433c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a433c-109">Type</span></span></th>
<th><span data-ttu-id="a433c-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="a433c-110">Required</span></span></th>
<th><span data-ttu-id="a433c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a433c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a433c-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="a433c-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="a433c-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="a433c-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="a433c-114">No</span><span class="sxs-lookup"><span data-stu-id="a433c-114">No</span></span><br/></td>
<td><span data-ttu-id="a433c-115">Este atributo solo es válido cuando el <strong>elemento Button</strong> es un elemento secundario <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>de QuickAccessToolbar.ApplicationDefaults.</strong></a></span><span class="sxs-lookup"><span data-stu-id="a433c-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="a433c-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a433c-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="a433c-117">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="a433c-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="a433c-118">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a433c-118">Default.</span></span> <br/> </dd> <span data-ttu-id="a433c-119"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="a433c-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a433c-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="a433c-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="a433c-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="a433c-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="a433c-122">No</span><span class="sxs-lookup"><span data-stu-id="a433c-122">No</span></span><br/></td>
<td><span data-ttu-id="a433c-123">Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a433c-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="a433c-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="a433c-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a433c-125">Cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="a433c-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="a433c-126">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="a433c-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="a433c-127">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a433c-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a433c-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a433c-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a433c-129">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="a433c-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a433c-130">No</span><span class="sxs-lookup"><span data-stu-id="a433c-130">No</span></span><br/></td>
<td><span data-ttu-id="a433c-131">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a433c-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="a433c-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="a433c-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a433c-133">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a433c-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a433c-134">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="a433c-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a433c-135">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a433c-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a433c-136">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a433c-136">Child elements</span></span>

<span data-ttu-id="a433c-137">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a433c-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a433c-138">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a433c-138">Parent elements</span></span>



| <span data-ttu-id="a433c-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="a433c-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a433c-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="a433c-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="a433c-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="a433c-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="a433c-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a433c-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="a433c-143">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="a433c-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="a433c-144">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="a433c-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="a433c-145">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="a433c-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="a433c-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a433c-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="a433c-147">**SplitButton.ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="a433c-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="a433c-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a433c-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="a433c-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a433c-149">Remarks</span></span>

<span data-ttu-id="a433c-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a433c-150">Optional.</span></span>

<span data-ttu-id="a433c-151">Puede producirse como máximo una vez para cada [**elemento SplitButton.ButtonItem.**](windowsribbon-element-splitbutton-buttonitem.md)</span><span class="sxs-lookup"><span data-stu-id="a433c-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="a433c-152">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults,**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) [**SplitButton**](windowsribbon-element-splitbutton.md) [**o SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="a433c-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="a433c-153">**Button** admite [los modos de](ribbon-applicationmodes.md) aplicación cuando se hospeda en la columna izquierda del menú aplicación.</span><span class="sxs-lookup"><span data-stu-id="a433c-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="a433c-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a433c-154">Examples</span></span>

<span data-ttu-id="a433c-155">En el ejemplo siguiente se muestra el marcado básico para **button**.</span><span class="sxs-lookup"><span data-stu-id="a433c-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="a433c-156">En esta sección de código se muestran las **declaraciones del** comando Button, con un [**grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el **elemento Button.**</span><span class="sxs-lookup"><span data-stu-id="a433c-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


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



<span data-ttu-id="a433c-157">En esta sección de código se muestran las **declaraciones del** control Button.</span><span class="sxs-lookup"><span data-stu-id="a433c-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="a433c-158">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a433c-158">Element information</span></span>

* <span data-ttu-id="a433c-159">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="a433c-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="a433c-160">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="a433c-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="a433c-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="a433c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a433c-162">Control de botón</span><span class="sxs-lookup"><span data-stu-id="a433c-162">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="a433c-163">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="a433c-163">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

