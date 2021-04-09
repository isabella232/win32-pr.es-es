---
title: CheckBox, elemento
description: Representa un control de casilla.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- CheckBox (elemento) cinta de Windows
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0af090058e0475f1997c681750009a12f4e5e7cd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104149066"
---
# <a name="checkbox-element"></a><span data-ttu-id="4d365-104">CheckBox, elemento</span><span class="sxs-lookup"><span data-stu-id="4d365-104">CheckBox element</span></span>

<span data-ttu-id="4d365-105">Representa un control de [casilla](windowsribbon-controls-checkbox.md) .</span><span class="sxs-lookup"><span data-stu-id="4d365-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="4d365-106">Uso</span><span class="sxs-lookup"><span data-stu-id="4d365-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="4d365-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4d365-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d365-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="4d365-108">Attribute</span></span></th>
<th><span data-ttu-id="4d365-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d365-109">Type</span></span></th>
<th><span data-ttu-id="4d365-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d365-110">Required</span></span></th>
<th><span data-ttu-id="4d365-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d365-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d365-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="4d365-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="4d365-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="4d365-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="4d365-114">No</span><span class="sxs-lookup"><span data-stu-id="4d365-114">No</span></span><br/></td>
<td><span data-ttu-id="4d365-115">Este atributo solo es válido cuando el elemento <strong>CheckBox</strong> es un elemento secundario de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d365-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="4d365-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="4d365-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4d365-117">La <strong>casilla</strong> no admite un estado terciario o indeterminado.</span><span class="sxs-lookup"><span data-stu-id="4d365-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="4d365-118">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="4d365-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="4d365-119">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4d365-119">Default.</span></span> <br/> </dd> <span data-ttu-id="4d365-120"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="4d365-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d365-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="4d365-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="4d365-122">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="4d365-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="4d365-123">No</span><span class="sxs-lookup"><span data-stu-id="4d365-123">No</span></span><br/></td>
<td><span data-ttu-id="4d365-124">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d365-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="4d365-125">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="4d365-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4d365-126">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="4d365-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="4d365-127">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="4d365-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="4d365-128">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4d365-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="4d365-129">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d365-129">Child elements</span></span>

<span data-ttu-id="4d365-130">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="4d365-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4d365-131">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4d365-131">Parent elements</span></span>



| <span data-ttu-id="4d365-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="4d365-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d365-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="4d365-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="4d365-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="4d365-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="4d365-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="4d365-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="4d365-136">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="4d365-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="4d365-137">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="4d365-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="4d365-138">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="4d365-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="4d365-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="4d365-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="4d365-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="4d365-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="4d365-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d365-141">Remarks</span></span>

<span data-ttu-id="4d365-142">Opcional o obligatorio, dependiendo del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="4d365-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="4d365-143">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="4d365-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="4d365-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d365-144">Examples</span></span>

<span data-ttu-id="4d365-145">En el ejemplo siguiente se muestra el marcado básico para el elemento **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4d365-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="4d365-146">En esta sección de código se muestran las declaraciones del comando **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4d365-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="4d365-147">En esta sección de código se muestran las declaraciones del control **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="4d365-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="4d365-148">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4d365-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="4d365-149">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d365-149">Minimum supported system</span></span><br/> | <span data-ttu-id="4d365-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d365-150">Windows 7</span></span> |
| <span data-ttu-id="4d365-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4d365-151">Can be empty</span></span>                        | <span data-ttu-id="4d365-152">Sí</span><span class="sxs-lookup"><span data-stu-id="4d365-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="4d365-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d365-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d365-154">Check Box (control)</span><span class="sxs-lookup"><span data-stu-id="4d365-154">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





