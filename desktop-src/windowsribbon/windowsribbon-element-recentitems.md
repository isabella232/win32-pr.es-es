---
title: Elemento RecentItems
description: Representa el control Elementos recientes en el menú De la aplicación.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444116"
---
# <a name="recentitems-element"></a><span data-ttu-id="20181-104">Elemento RecentItems</span><span class="sxs-lookup"><span data-stu-id="20181-104">RecentItems element</span></span>

<span data-ttu-id="20181-105">Representa el [control Elementos recientes](windowsribbon-controls-recentitems.md) en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="20181-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="20181-106">Uso</span><span class="sxs-lookup"><span data-stu-id="20181-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="20181-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="20181-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20181-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="20181-108">Attribute</span></span></th>
<th><span data-ttu-id="20181-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="20181-109">Type</span></span></th>
<th><span data-ttu-id="20181-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="20181-110">Required</span></span></th>
<th><span data-ttu-id="20181-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="20181-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20181-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="20181-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="20181-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="20181-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="20181-114">No</span><span class="sxs-lookup"><span data-stu-id="20181-114">No</span></span><br/></td>
<td><span data-ttu-id="20181-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="20181-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="20181-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="20181-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="20181-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="20181-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="20181-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="20181-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="20181-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="20181-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20181-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="20181-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="20181-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="20181-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="20181-122">No</span><span class="sxs-lookup"><span data-stu-id="20181-122">No</span></span><br/></td>
<td><span data-ttu-id="20181-123">Restringido a uno de los siguientes valores (0 y 1 no son válidos):</span><span class="sxs-lookup"><span data-stu-id="20181-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="20181-124">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="20181-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="20181-125">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="20181-125">Default.</span></span> <br/> </dd> <span data-ttu-id="20181-126"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="20181-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20181-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="20181-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="20181-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="20181-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="20181-129">No</span><span class="sxs-lookup"><span data-stu-id="20181-129">No</span></span><br/></td>
<td><span data-ttu-id="20181-130">Número de elementos recientes que se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="20181-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="20181-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="20181-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="20181-132">Valor entero de 0 o mayor.</span><span class="sxs-lookup"><span data-stu-id="20181-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="20181-133">El valor predeterminado <strong>es 10.</strong></span><span class="sxs-lookup"><span data-stu-id="20181-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="20181-134">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20181-134">Child elements</span></span>

<span data-ttu-id="20181-135">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="20181-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="20181-136">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="20181-136">Parent elements</span></span>



| <span data-ttu-id="20181-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="20181-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20181-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="20181-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="20181-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20181-139">Remarks</span></span>

<span data-ttu-id="20181-140">Necesario.</span><span class="sxs-lookup"><span data-stu-id="20181-140">Required.</span></span>

<span data-ttu-id="20181-141">Debe producirse exactamente una vez [**para cada elemento ApplicationMenu.RecentItems.**](windowsribbon-element-applicationmenu-recentitems.md)</span><span class="sxs-lookup"><span data-stu-id="20181-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="20181-142">El [control Elementos recientes](windowsribbon-controls-recentitems.md) muestra la lista de elementos usados más recientemente (MRU) de la aplicación Ribbon.</span><span class="sxs-lookup"><span data-stu-id="20181-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="20181-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="20181-143">Examples</span></span>

<span data-ttu-id="20181-144">En el ejemplo siguiente se muestra el marcado básico para el control [Elementos recientes.](windowsribbon-controls-recentitems.md)</span><span class="sxs-lookup"><span data-stu-id="20181-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="20181-145">En el ejemplo siguiente se muestra **una declaración RecentItems** Command.</span><span class="sxs-lookup"><span data-stu-id="20181-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="20181-146">En el ejemplo siguiente se muestra la **declaración de controles RecentItems** asociada.</span><span class="sxs-lookup"><span data-stu-id="20181-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="20181-147">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="20181-147">Element information</span></span>

* <span data-ttu-id="20181-148">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="20181-148">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="20181-149">**Puede estar vacío:** Sí</span><span class="sxs-lookup"><span data-stu-id="20181-149">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="20181-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="20181-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20181-151">Control Menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="20181-151">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="20181-152">Control Elementos recientes</span><span class="sxs-lookup"><span data-stu-id="20181-152">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





