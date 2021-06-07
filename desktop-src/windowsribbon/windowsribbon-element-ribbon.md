---
title: Elemento Ribbon
description: Representa el control de la cinta de opciones en la vista de cinta de opciones.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Cinta de opciones de Windows, elemento
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445006"
---
# <a name="ribbon-element"></a><span data-ttu-id="36bfb-104">Elemento Ribbon</span><span class="sxs-lookup"><span data-stu-id="36bfb-104">Ribbon element</span></span>

<span data-ttu-id="36bfb-105">Representa el control de la cinta de opciones en la vista de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="36bfb-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="36bfb-106">Uso</span><span class="sxs-lookup"><span data-stu-id="36bfb-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="36bfb-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="36bfb-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36bfb-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="36bfb-108">Attribute</span></span></th>
<th><span data-ttu-id="36bfb-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="36bfb-109">Type</span></span></th>
<th><span data-ttu-id="36bfb-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="36bfb-110">Required</span></span></th>
<th><span data-ttu-id="36bfb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="36bfb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bfb-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="36bfb-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="36bfb-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="36bfb-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="36bfb-114">No</span><span class="sxs-lookup"><span data-stu-id="36bfb-114">No</span></span><br/></td>
<td><span data-ttu-id="36bfb-115"><dt><span></span><span></span><strong></strong> (Pequeño)</span><span class="sxs-lookup"><span data-stu-id="36bfb-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="36bfb-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="36bfb-116">Default.</span></span> <br/> </dd> <span data-ttu-id="36bfb-117"><dt><span></span><span></span><strong></strong> (Medio)</span><span class="sxs-lookup"><span data-stu-id="36bfb-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="36bfb-118"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="36bfb-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bfb-119"><strong>Nombre</strong></span><span class="sxs-lookup"><span data-stu-id="36bfb-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="36bfb-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="36bfb-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="36bfb-121">No</span><span class="sxs-lookup"><span data-stu-id="36bfb-121">No</span></span><br/></td>
<td><span data-ttu-id="36bfb-122">Se usa para anotar el elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="36bfb-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="36bfb-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="36bfb-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="36bfb-124">Cualquier secuencia de cero o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="36bfb-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="36bfb-125">La longitud máxima es sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="36bfb-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="36bfb-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="36bfb-126">Child elements</span></span>



| <span data-ttu-id="36bfb-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="36bfb-127">Element</span></span>                                                                                         | <span data-ttu-id="36bfb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="36bfb-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="36bfb-129">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="36bfb-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="36bfb-130">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="36bfb-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="36bfb-131">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="36bfb-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="36bfb-132">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="36bfb-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="36bfb-133">**Ribbon.HelpButton**</span><span class="sxs-lookup"><span data-stu-id="36bfb-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="36bfb-134">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="36bfb-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="36bfb-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="36bfb-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="36bfb-136">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="36bfb-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="36bfb-137">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="36bfb-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="36bfb-138">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="36bfb-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="36bfb-139">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="36bfb-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="36bfb-140">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="36bfb-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="36bfb-141">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="36bfb-141">Parent elements</span></span>



| <span data-ttu-id="36bfb-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="36bfb-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="36bfb-143">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="36bfb-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="36bfb-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36bfb-144">Remarks</span></span>

<span data-ttu-id="36bfb-145">Necesario.</span><span class="sxs-lookup"><span data-stu-id="36bfb-145">Required.</span></span>

<span data-ttu-id="36bfb-146">Debe producirse exactamente una vez para [**cada elemento Application.Views.**](windowsribbon-element-application-views.md)</span><span class="sxs-lookup"><span data-stu-id="36bfb-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="36bfb-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="36bfb-147">Examples</span></span>

<span data-ttu-id="36bfb-148">En el ejemplo siguiente se muestra el marcado básico para una vista **de cinta** de opciones.</span><span class="sxs-lookup"><span data-stu-id="36bfb-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="36bfb-149">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="36bfb-149">Element information</span></span>




* <span data-ttu-id="36bfb-150">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="36bfb-150">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="36bfb-151">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="36bfb-151">**Can be empty**: No</span></span>



 

 





