---
title: Elemento ApplicationMenu
description: Representa el menú de la aplicación. | Elemento ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Elemento ApplicationMenu de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e535fbcc09a404ad7dd5a4019438f4513f5c77c6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443056"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="041ed-105">Elemento ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="041ed-105">ApplicationMenu element</span></span>

<span data-ttu-id="041ed-106">Representa el [menú de la aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="041ed-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="041ed-107">Uso</span><span class="sxs-lookup"><span data-stu-id="041ed-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="041ed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="041ed-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="041ed-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="041ed-109">Attribute</span></span></th>
<th><span data-ttu-id="041ed-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="041ed-110">Type</span></span></th>
<th><span data-ttu-id="041ed-111">Requerido</span><span class="sxs-lookup"><span data-stu-id="041ed-111">Required</span></span></th>
<th><span data-ttu-id="041ed-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="041ed-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="041ed-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="041ed-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="041ed-114">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="041ed-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="041ed-115">No</span><span class="sxs-lookup"><span data-stu-id="041ed-115">No</span></span><br/></td>
<td><span data-ttu-id="041ed-116">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="041ed-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="041ed-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="041ed-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="041ed-118">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="041ed-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="041ed-119">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="041ed-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="041ed-120">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="041ed-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="041ed-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="041ed-121">Child elements</span></span>



| <span data-ttu-id="041ed-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="041ed-122">Element</span></span>                                                                                             | <span data-ttu-id="041ed-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="041ed-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="041ed-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="041ed-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="041ed-125">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="041ed-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="041ed-126">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="041ed-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="041ed-127">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="041ed-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="041ed-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="041ed-128">Parent elements</span></span>



| <span data-ttu-id="041ed-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="041ed-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="041ed-130">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="041ed-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="041ed-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="041ed-131">Remarks</span></span>

<span data-ttu-id="041ed-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="041ed-132">Required.</span></span>

<span data-ttu-id="041ed-133">Debe producirse exactamente una vez para [**cada Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="041ed-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="041ed-134">Los elementos secundarios del **elemento ApplicationMenu** deben producirse en el orden especificado:</span><span class="sxs-lookup"><span data-stu-id="041ed-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="041ed-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="041ed-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="041ed-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="041ed-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="041ed-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="041ed-137">Examples</span></span>

<span data-ttu-id="041ed-138">En el ejemplo siguiente se muestra el marcado básico para el [menú de la aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="041ed-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="041ed-139">En esta sección de código se muestran las declaraciones del comando **ApplicationMenu.**</span><span class="sxs-lookup"><span data-stu-id="041ed-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="041ed-140">En esta sección de código se muestran las declaraciones del control **ApplicationMenu.**</span><span class="sxs-lookup"><span data-stu-id="041ed-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a><span data-ttu-id="041ed-141">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="041ed-141">Element information</span></span>

* <span data-ttu-id="041ed-142">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="041ed-142">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="041ed-143">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="041ed-143">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="041ed-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="041ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041ed-145">Control Menú de la aplicación</span><span class="sxs-lookup"><span data-stu-id="041ed-145">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





