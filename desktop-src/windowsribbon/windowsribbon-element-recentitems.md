---
title: Elemento RecentItems
description: Representa el control de elementos recientes en el menú de la aplicación.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems cinta de opciones de Windows
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104077259"
---
# <a name="recentitems-element"></a><span data-ttu-id="66f8d-104">Elemento RecentItems</span><span class="sxs-lookup"><span data-stu-id="66f8d-104">RecentItems element</span></span>

<span data-ttu-id="66f8d-105">Representa el control de [elementos recientes](windowsribbon-controls-recentitems.md) en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="66f8d-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="66f8d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="66f8d-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="66f8d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="66f8d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66f8d-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="66f8d-108">Attribute</span></span></th>
<th><span data-ttu-id="66f8d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="66f8d-109">Type</span></span></th>
<th><span data-ttu-id="66f8d-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="66f8d-110">Required</span></span></th>
<th><span data-ttu-id="66f8d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="66f8d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66f8d-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="66f8d-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="66f8d-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="66f8d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="66f8d-114">No</span><span class="sxs-lookup"><span data-stu-id="66f8d-114">No</span></span><br/></td>
<td><span data-ttu-id="66f8d-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="66f8d-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="66f8d-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="66f8d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="66f8d-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="66f8d-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="66f8d-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="66f8d-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="66f8d-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="66f8d-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66f8d-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="66f8d-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="66f8d-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="66f8d-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="66f8d-122">No</span><span class="sxs-lookup"><span data-stu-id="66f8d-122">No</span></span><br/></td>
<td><span data-ttu-id="66f8d-123">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="66f8d-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="66f8d-124">
<dt><span></span><span></span><strong></strong> reales</span><span class="sxs-lookup"><span data-stu-id="66f8d-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="66f8d-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="66f8d-125">Default.</span></span> <br/> </dd> <span data-ttu-id="66f8d-126"><dt><span></span><span></span><strong></strong> es</span><span class="sxs-lookup"><span data-stu-id="66f8d-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66f8d-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="66f8d-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="66f8d-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="66f8d-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="66f8d-129">No</span><span class="sxs-lookup"><span data-stu-id="66f8d-129">No</span></span><br/></td>
<td><span data-ttu-id="66f8d-130">Número de elementos recientes que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="66f8d-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="66f8d-131">
<dt><span></span><span></span><strong></strong> (XS: nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="66f8d-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="66f8d-132">Valor entero de 0 o superior.</span><span class="sxs-lookup"><span data-stu-id="66f8d-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="66f8d-133">El valor predeterminado es <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="66f8d-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="66f8d-134">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66f8d-134">Child elements</span></span>

<span data-ttu-id="66f8d-135">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="66f8d-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="66f8d-136">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="66f8d-136">Parent elements</span></span>



| <span data-ttu-id="66f8d-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="66f8d-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66f8d-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="66f8d-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="66f8d-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66f8d-139">Remarks</span></span>

<span data-ttu-id="66f8d-140">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66f8d-140">Required.</span></span>

<span data-ttu-id="66f8d-141">Debe aparecer exactamente una vez para cada elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="66f8d-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="66f8d-142">El control [elementos recientes](windowsribbon-controls-recentitems.md) muestra la lista de elementos usados más recientemente (MRU) de la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="66f8d-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="66f8d-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="66f8d-143">Examples</span></span>

<span data-ttu-id="66f8d-144">En el ejemplo siguiente se muestra el marcado básico para el control de [elementos recientes](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="66f8d-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="66f8d-145">En el ejemplo siguiente se muestra una declaración de comando **RecentItems** .</span><span class="sxs-lookup"><span data-stu-id="66f8d-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="66f8d-146">En el ejemplo siguiente se muestra la declaración de controles **RecentItems** asociados.</span><span class="sxs-lookup"><span data-stu-id="66f8d-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="66f8d-147">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="66f8d-147">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="66f8d-148">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66f8d-148">Minimum supported system</span></span><br/> | <span data-ttu-id="66f8d-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66f8d-149">Windows 7</span></span> |
| <span data-ttu-id="66f8d-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="66f8d-150">Can be empty</span></span>                        | <span data-ttu-id="66f8d-151">Sí</span><span class="sxs-lookup"><span data-stu-id="66f8d-151">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="66f8d-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="66f8d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f8d-153">Control de menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="66f8d-153">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="66f8d-154">Control de elementos recientes</span><span class="sxs-lookup"><span data-stu-id="66f8d-154">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





