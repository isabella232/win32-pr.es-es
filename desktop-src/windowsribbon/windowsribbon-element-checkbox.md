---
title: Elemento CheckBox
description: Representa un control Casilla.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- Cinta de opciones de Windows del elemento CheckBox
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9357337e569f43b14c34798c9c6e8da4b7b10b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443046"
---
# <a name="checkbox-element"></a><span data-ttu-id="db92a-104">Elemento CheckBox</span><span class="sxs-lookup"><span data-stu-id="db92a-104">CheckBox element</span></span>

<span data-ttu-id="db92a-105">Representa un [control Casilla.](windowsribbon-controls-checkbox.md)</span><span class="sxs-lookup"><span data-stu-id="db92a-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="db92a-106">Uso</span><span class="sxs-lookup"><span data-stu-id="db92a-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="db92a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="db92a-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db92a-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="db92a-108">Attribute</span></span></th>
<th><span data-ttu-id="db92a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="db92a-109">Type</span></span></th>
<th><span data-ttu-id="db92a-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="db92a-110">Required</span></span></th>
<th><span data-ttu-id="db92a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="db92a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db92a-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="db92a-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="db92a-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="db92a-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="db92a-114">No</span><span class="sxs-lookup"><span data-stu-id="db92a-114">No</span></span><br/></td>
<td><span data-ttu-id="db92a-115">Este atributo solo es válido cuando el <strong>elemento CheckBox</strong> es un elemento secundario <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>de QuickAccessToolbar.ApplicationDefaults.</strong></a></span><span class="sxs-lookup"><span data-stu-id="db92a-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="db92a-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="db92a-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="db92a-117"><strong>CheckBox</strong> no admite un estado terciario o indeterminado.</span><span class="sxs-lookup"><span data-stu-id="db92a-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="db92a-118">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="db92a-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="db92a-119">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="db92a-119">Default.</span></span> <br/> </dd> <span data-ttu-id="db92a-120"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="db92a-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db92a-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="db92a-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="db92a-122">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="db92a-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="db92a-123">No</span><span class="sxs-lookup"><span data-stu-id="db92a-123">No</span></span><br/></td>
<td><span data-ttu-id="db92a-124">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="db92a-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="db92a-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="db92a-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="db92a-126">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="db92a-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="db92a-127">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="db92a-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="db92a-128">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="db92a-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="db92a-129">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="db92a-129">Child elements</span></span>

<span data-ttu-id="db92a-130">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="db92a-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="db92a-131">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="db92a-131">Parent elements</span></span>



| <span data-ttu-id="db92a-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="db92a-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db92a-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="db92a-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="db92a-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="db92a-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="db92a-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="db92a-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="db92a-136">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="db92a-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="db92a-137">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="db92a-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="db92a-138">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="db92a-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="db92a-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="db92a-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="db92a-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="db92a-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="db92a-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db92a-141">Remarks</span></span>

<span data-ttu-id="db92a-142">Opcional o obligatorio, en función del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="db92a-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="db92a-143">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults,**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) [**SplitButton**](windowsribbon-element-splitbutton.md) [**o SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="db92a-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="db92a-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="db92a-144">Examples</span></span>

<span data-ttu-id="db92a-145">En el ejemplo siguiente se muestra el marcado básico para el **elemento CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="db92a-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="db92a-146">En esta sección de código se muestran las declaraciones del comando **CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="db92a-146">This section of code shows the **CheckBox** Command declarations.</span></span>


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



<span data-ttu-id="db92a-147">En esta sección de código se muestran las declaraciones del control **CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="db92a-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="db92a-148">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="db92a-148">Element information</span></span>

* <span data-ttu-id="db92a-149">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="db92a-149">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="db92a-150">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="db92a-150">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="db92a-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="db92a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db92a-152">Check Box (control)</span><span class="sxs-lookup"><span data-stu-id="db92a-152">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





