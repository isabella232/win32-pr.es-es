---
title: ToggleButton (elemento)
description: Representa un control de botón de alternancia.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Barra de herramientas de Windows de elemento ToggleButton
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104358640"
---
# <a name="togglebutton-element"></a><span data-ttu-id="631c2-104">ToggleButton (elemento)</span><span class="sxs-lookup"><span data-stu-id="631c2-104">ToggleButton element</span></span>

<span data-ttu-id="631c2-105">Representa un control de [botón de alternancia](windowsribbon-controls-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="631c2-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="631c2-106">Uso</span><span class="sxs-lookup"><span data-stu-id="631c2-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="631c2-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="631c2-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="631c2-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="631c2-108">Attribute</span></span></th>
<th><span data-ttu-id="631c2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="631c2-109">Type</span></span></th>
<th><span data-ttu-id="631c2-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="631c2-110">Required</span></span></th>
<th><span data-ttu-id="631c2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="631c2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="631c2-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="631c2-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="631c2-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="631c2-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="631c2-114">No</span><span class="sxs-lookup"><span data-stu-id="631c2-114">No</span></span><br/></td>
<td><span data-ttu-id="631c2-115">Este atributo solo es válido cuando el elemento <strong>ToggleButton</strong> es un elemento secundario de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="631c2-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="631c2-116">Restringido a uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="631c2-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="631c2-117">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="631c2-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="631c2-118">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="631c2-118">Default.</span></span> <br/> </dd> <span data-ttu-id="631c2-119"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="631c2-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="631c2-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="631c2-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="631c2-121">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="631c2-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="631c2-122">No</span><span class="sxs-lookup"><span data-stu-id="631c2-122">No</span></span><br/></td>
<td><span data-ttu-id="631c2-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="631c2-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="631c2-124">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="631c2-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="631c2-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="631c2-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="631c2-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="631c2-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="631c2-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="631c2-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="631c2-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="631c2-128">Child elements</span></span>

<span data-ttu-id="631c2-129">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="631c2-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="631c2-130">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="631c2-130">Parent elements</span></span>



| <span data-ttu-id="631c2-131">Elemento</span><span class="sxs-lookup"><span data-stu-id="631c2-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="631c2-132">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="631c2-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="631c2-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="631c2-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="631c2-134">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="631c2-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="631c2-135">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="631c2-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="631c2-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="631c2-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="631c2-137">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="631c2-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="631c2-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="631c2-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="631c2-139">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="631c2-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="631c2-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="631c2-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="631c2-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="631c2-141">Remarks</span></span>

<span data-ttu-id="631c2-142">Opcional o obligatorio, dependiendo del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="631c2-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="631c2-143">Puede aparecer como máximo una vez por cada elemento [**splitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="631c2-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="631c2-144">Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="631c2-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="631c2-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="631c2-145">Examples</span></span>

<span data-ttu-id="631c2-146">En el ejemplo siguiente se muestra el marcado básico para el elemento **ToggleButton** .</span><span class="sxs-lookup"><span data-stu-id="631c2-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="631c2-147">En esta sección de código se muestra una declaración de elemento **ToggleButton** dentro del elemento [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .</span><span class="sxs-lookup"><span data-stu-id="631c2-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="631c2-148">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="631c2-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="631c2-149">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="631c2-149">Minimum supported system</span></span><br/> | <span data-ttu-id="631c2-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="631c2-150">Windows 7</span></span> |
| <span data-ttu-id="631c2-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="631c2-151">Can be empty</span></span>                        | <span data-ttu-id="631c2-152">Sí</span><span class="sxs-lookup"><span data-stu-id="631c2-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="631c2-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="631c2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631c2-154">Control de botón de alternancia</span><span class="sxs-lookup"><span data-stu-id="631c2-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





