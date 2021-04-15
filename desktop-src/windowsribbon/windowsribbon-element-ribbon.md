---
title: Elemento Ribbon
description: Representa el control de la cinta de opciones en la vista de la cinta.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Cinta de opciones de Windows (elemento)
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714279"
---
# <a name="ribbon-element"></a><span data-ttu-id="29a91-104">Elemento Ribbon</span><span class="sxs-lookup"><span data-stu-id="29a91-104">Ribbon element</span></span>

<span data-ttu-id="29a91-105">Representa el control de la cinta de opciones en la vista de la cinta.</span><span class="sxs-lookup"><span data-stu-id="29a91-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="29a91-106">Uso</span><span class="sxs-lookup"><span data-stu-id="29a91-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="29a91-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="29a91-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29a91-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="29a91-108">Attribute</span></span></th>
<th><span data-ttu-id="29a91-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="29a91-109">Type</span></span></th>
<th><span data-ttu-id="29a91-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="29a91-110">Required</span></span></th>
<th><span data-ttu-id="29a91-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="29a91-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29a91-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="29a91-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="29a91-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="29a91-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="29a91-114">No</span><span class="sxs-lookup"><span data-stu-id="29a91-114">No</span></span><br/></td>
<td><span data-ttu-id="29a91-115"><dt><span></span><span></span><strong></strong> Pequeño</span><span class="sxs-lookup"><span data-stu-id="29a91-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="29a91-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="29a91-116">Default.</span></span> <br/> </dd> <span data-ttu-id="29a91-117"><dt><span></span><span></span><strong></strong> Medio</span><span class="sxs-lookup"><span data-stu-id="29a91-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="29a91-118"><dt><span></span><span></span><strong></strong> Amplíe</span><span class="sxs-lookup"><span data-stu-id="29a91-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29a91-119"><strong>Nombre</strong></span><span class="sxs-lookup"><span data-stu-id="29a91-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="29a91-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="29a91-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="29a91-121">No</span><span class="sxs-lookup"><span data-stu-id="29a91-121">No</span></span><br/></td>
<td><span data-ttu-id="29a91-122">Se utiliza para anotar el elemento Command.</span><span class="sxs-lookup"><span data-stu-id="29a91-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="29a91-123">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="29a91-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="29a91-124">Cualquier secuencia de cero o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="29a91-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="29a91-125">La longitud máxima es sin límite.</span><span class="sxs-lookup"><span data-stu-id="29a91-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="29a91-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="29a91-126">Child elements</span></span>



| <span data-ttu-id="29a91-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="29a91-127">Element</span></span>                                                                                         | <span data-ttu-id="29a91-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="29a91-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="29a91-129">**Ribbon. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="29a91-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="29a91-130">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="29a91-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="29a91-131">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="29a91-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="29a91-132">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="29a91-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="29a91-133">**Ribbon. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="29a91-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="29a91-134">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="29a91-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="29a91-135">**Ribbon. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="29a91-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="29a91-136">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="29a91-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="29a91-137">**Ribbon. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="29a91-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="29a91-138">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="29a91-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="29a91-139">**Cinta. pestañas**</span><span class="sxs-lookup"><span data-stu-id="29a91-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="29a91-140">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="29a91-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="29a91-141">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="29a91-141">Parent elements</span></span>



| <span data-ttu-id="29a91-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="29a91-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="29a91-143">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="29a91-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="29a91-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29a91-144">Remarks</span></span>

<span data-ttu-id="29a91-145">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="29a91-145">Required.</span></span>

<span data-ttu-id="29a91-146">Debe aparecer exactamente una vez para cada elemento [**Application. views**](windowsribbon-element-application-views.md) .</span><span class="sxs-lookup"><span data-stu-id="29a91-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="29a91-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="29a91-147">Examples</span></span>

<span data-ttu-id="29a91-148">En el ejemplo siguiente se muestra el marcado básico de una vista de **la cinta** de opciones.</span><span class="sxs-lookup"><span data-stu-id="29a91-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="29a91-149">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="29a91-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="29a91-150">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29a91-150">Minimum supported system</span></span><br/> | <span data-ttu-id="29a91-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="29a91-151">Windows 7</span></span> |
| <span data-ttu-id="29a91-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="29a91-152">Can be empty</span></span>                        | <span data-ttu-id="29a91-153">No</span><span class="sxs-lookup"><span data-stu-id="29a91-153">No</span></span>        |



 

 





