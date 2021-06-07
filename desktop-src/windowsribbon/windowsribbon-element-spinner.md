---
title: Elemento Spinner
description: Representa un control Spinner.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Cinta de opciones de Windows del elemento Spinner
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1ec2e074271e125199ddfd4ff8fac7b2af80c33
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444816"
---
# <a name="spinner-element"></a><span data-ttu-id="57b5c-104">Elemento Spinner</span><span class="sxs-lookup"><span data-stu-id="57b5c-104">Spinner element</span></span>

<span data-ttu-id="57b5c-105">Representa un [control Spinner.](windowsribbon-controls-spinner.md)</span><span class="sxs-lookup"><span data-stu-id="57b5c-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="57b5c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="57b5c-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="57b5c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="57b5c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57b5c-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="57b5c-108">Attribute</span></span></th>
<th><span data-ttu-id="57b5c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="57b5c-109">Type</span></span></th>
<th><span data-ttu-id="57b5c-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="57b5c-110">Required</span></span></th>
<th><span data-ttu-id="57b5c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="57b5c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57b5c-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="57b5c-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="57b5c-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="57b5c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="57b5c-114">No</span><span class="sxs-lookup"><span data-stu-id="57b5c-114">No</span></span><br/></td>
<td><span data-ttu-id="57b5c-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="57b5c-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="57b5c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="57b5c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="57b5c-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="57b5c-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="57b5c-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="57b5c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="57b5c-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="57b5c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="57b5c-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="57b5c-120">Child elements</span></span>

<span data-ttu-id="57b5c-121">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="57b5c-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="57b5c-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="57b5c-122">Parent elements</span></span>



| <span data-ttu-id="57b5c-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="57b5c-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="57b5c-124">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="57b5c-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="57b5c-125">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="57b5c-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="57b5c-126">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="57b5c-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="57b5c-127">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="57b5c-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="57b5c-128">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="57b5c-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="57b5c-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57b5c-129">Remarks</span></span>

<span data-ttu-id="57b5c-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="57b5c-130">Optional.</span></span>

<span data-ttu-id="57b5c-131">Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**o Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="57b5c-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="57b5c-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="57b5c-132">Examples</span></span>

<span data-ttu-id="57b5c-133">En el ejemplo siguiente se muestra el marcado básico para [spinner.](windowsribbon-controls-spinner.md)</span><span class="sxs-lookup"><span data-stu-id="57b5c-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="57b5c-134">En esta sección de código se muestran las declaraciones de comando de **spinner,** con un elemento [**Group**](windowsribbon-element-group.md) que funciona como contenedor primario para el **elemento Spinner.**</span><span class="sxs-lookup"><span data-stu-id="57b5c-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="57b5c-135">En esta sección de código se muestran las declaraciones de control **Spinner.**</span><span class="sxs-lookup"><span data-stu-id="57b5c-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="57b5c-136">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="57b5c-136">Element information</span></span>

- <span data-ttu-id="57b5c-137">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="57b5c-137">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="57b5c-138">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="57b5c-138">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="57b5c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="57b5c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b5c-140">Control spinner</span><span class="sxs-lookup"><span data-stu-id="57b5c-140">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





