---
title: ComboBox (elemento)
description: Representa un control de cuadro combinado.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Elemento ComboBox cinta de Windows
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105704893"
---
# <a name="combobox-element"></a><span data-ttu-id="9024d-104">ComboBox (elemento)</span><span class="sxs-lookup"><span data-stu-id="9024d-104">ComboBox element</span></span>

<span data-ttu-id="9024d-105">Representa un control de [cuadro combinado](windowsribbon-controls-combobox.md) .</span><span class="sxs-lookup"><span data-stu-id="9024d-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="9024d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="9024d-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="9024d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="9024d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9024d-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="9024d-108">Attribute</span></span></th>
<th><span data-ttu-id="9024d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9024d-109">Type</span></span></th>
<th><span data-ttu-id="9024d-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9024d-110">Required</span></span></th>
<th><span data-ttu-id="9024d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9024d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9024d-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="9024d-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="9024d-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="9024d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="9024d-114">No</span><span class="sxs-lookup"><span data-stu-id="9024d-114">No</span></span><br/></td>
<td><span data-ttu-id="9024d-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9024d-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="9024d-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="9024d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="9024d-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9024d-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="9024d-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="9024d-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="9024d-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9024d-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9024d-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="9024d-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="9024d-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="9024d-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="9024d-122">No</span><span class="sxs-lookup"><span data-stu-id="9024d-122">No</span></span><br/></td>
<td><span data-ttu-id="9024d-123">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9024d-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="9024d-124">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="9024d-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9024d-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9024d-125">Default.</span></span> <br/> </dd> <span data-ttu-id="9024d-126"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="9024d-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9024d-127"><strong>IsEditable</strong></span><span class="sxs-lookup"><span data-stu-id="9024d-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="9024d-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="9024d-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="9024d-129">No</span><span class="sxs-lookup"><span data-stu-id="9024d-129">No</span></span><br/></td>
<td><span data-ttu-id="9024d-130">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="9024d-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="9024d-131">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="9024d-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="9024d-132">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9024d-132">Default.</span></span> <br/> </dd> <span data-ttu-id="9024d-133"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="9024d-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9024d-134"><strong>ResizeType</strong></span><span class="sxs-lookup"><span data-stu-id="9024d-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="9024d-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="9024d-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="9024d-136">No</span><span class="sxs-lookup"><span data-stu-id="9024d-136">No</span></span><br/></td>
<td><span data-ttu-id="9024d-137"><dt><span></span><span></span><strong></strong> (NoResize)</span><span class="sxs-lookup"><span data-stu-id="9024d-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="9024d-138">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9024d-138">Default.</span></span> <br/> </dd> <span data-ttu-id="9024d-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span><span class="sxs-lookup"><span data-stu-id="9024d-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9024d-140">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9024d-140">Child elements</span></span>

<span data-ttu-id="9024d-141">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9024d-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9024d-142">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9024d-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9024d-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="9024d-143">Element</span></span></th>
<th><span data-ttu-id="9024d-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="9024d-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9024d-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9024d-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9024d-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9024d-148"><a href="windowsribbon-element-group.md"><strong>Group (Grupo)</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9024d-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="9024d-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="9024d-151">Windows 8 y versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="9024d-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9024d-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="9024d-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="9024d-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9024d-153">Remarks</span></span>

<span data-ttu-id="9024d-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9024d-154">Optional.</span></span>

<span data-ttu-id="9024d-155">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="9024d-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="9024d-156">Dado que el **cuadro combinado** es exclusivamente una galería de elementos, no admite elementos de comando.</span><span class="sxs-lookup"><span data-stu-id="9024d-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="9024d-157">También es el único control de la galería que no admite un espacio de comandos (una colección de comandos que se declaran en el marcado y que se enumeran en la parte inferior de una galería de elementos o una galería de comandos).</span><span class="sxs-lookup"><span data-stu-id="9024d-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="9024d-158">Para obtener más información, vea [trabajar con galerías](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="9024d-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="9024d-159">En la captura de pantalla siguiente se muestra un control de [cuadro combinado](windowsribbon-controls-combobox.md) de la cinta de opciones de Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="9024d-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![captura de pantalla de un control ComboBox en la cinta de opciones de Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="9024d-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9024d-161">Examples</span></span>

<span data-ttu-id="9024d-162">En los siguientes ejemplos se muestra el marcado básico para el **cuadro combinado**.</span><span class="sxs-lookup"><span data-stu-id="9024d-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="9024d-163">En esta sección de código se muestran las declaraciones de comandos de **ComboBox** , con un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario del elemento **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="9024d-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="9024d-164">En esta sección de código se muestran las declaraciones del control **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="9024d-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="9024d-165">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9024d-165">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9024d-166">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9024d-166">Minimum supported system</span></span><br/> | <span data-ttu-id="9024d-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9024d-167">Windows 7</span></span> |
| <span data-ttu-id="9024d-168">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9024d-168">Can be empty</span></span>                        | <span data-ttu-id="9024d-169">Sí</span><span class="sxs-lookup"><span data-stu-id="9024d-169">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="9024d-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9024d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9024d-171">Combo Box (control)</span><span class="sxs-lookup"><span data-stu-id="9024d-171">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="9024d-172">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="9024d-172">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





