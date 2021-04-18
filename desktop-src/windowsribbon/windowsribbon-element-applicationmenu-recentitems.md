---
title: Propiedad ApplicationMenu. RecentItems
description: Representa un contenedor para el control de elementos recientes en el menú de la aplicación.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- ApplicationMenu. RecentItems (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422348"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="6344f-104">Propiedad ApplicationMenu. RecentItems</span><span class="sxs-lookup"><span data-stu-id="6344f-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="6344f-105">Representa un contenedor para el control de [elementos recientes](windowsribbon-controls-recentitems.md) en el menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="6344f-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="6344f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="6344f-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="6344f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="6344f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6344f-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="6344f-108">Attribute</span></span></th>
<th><span data-ttu-id="6344f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6344f-109">Type</span></span></th>
<th><span data-ttu-id="6344f-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6344f-110">Required</span></span></th>
<th><span data-ttu-id="6344f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6344f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6344f-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6344f-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6344f-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="6344f-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6344f-114">No</span><span class="sxs-lookup"><span data-stu-id="6344f-114">No</span></span><br/></td>
<td><span data-ttu-id="6344f-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6344f-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6344f-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="6344f-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6344f-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="6344f-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6344f-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="6344f-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6344f-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6344f-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6344f-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6344f-120">Child elements</span></span>



| <span data-ttu-id="6344f-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="6344f-121">Element</span></span>                                                             | <span data-ttu-id="6344f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6344f-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="6344f-123">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="6344f-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="6344f-124">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="6344f-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6344f-125">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6344f-125">Parent elements</span></span>



| <span data-ttu-id="6344f-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="6344f-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="6344f-127">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="6344f-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6344f-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6344f-128">Remarks</span></span>

<span data-ttu-id="6344f-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6344f-129">Optional.</span></span>

<span data-ttu-id="6344f-130">Puede aparecer como máximo una vez por cada elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="6344f-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="6344f-131">El control [elementos recientes](windowsribbon-controls-recentitems.md) muestra la lista de elementos usados más recientemente (MRU) de la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="6344f-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="6344f-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6344f-132">Examples</span></span>

<span data-ttu-id="6344f-133">En el ejemplo siguiente se muestra el marcado básico para el control de [elementos recientes](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="6344f-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="6344f-134">En el ejemplo siguiente se muestra una declaración de comando [**RecentItems**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="6344f-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="6344f-135">En el ejemplo siguiente se muestra la declaración de controles asociados **ApplicationMenu. RecentItems** y [**RecentItems**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="6344f-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="6344f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6344f-136">Requirements</span></span>



| <span data-ttu-id="6344f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6344f-137">Requirement</span></span> | <span data-ttu-id="6344f-138">Value</span><span class="sxs-lookup"><span data-stu-id="6344f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6344f-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6344f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6344f-140">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6344f-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6344f-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6344f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6344f-142">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6344f-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6344f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6344f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6344f-144">Control de menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6344f-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="6344f-145">Control de elementos recientes</span><span class="sxs-lookup"><span data-stu-id="6344f-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





