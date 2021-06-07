---
title: Tab (Elemento)
description: Representa una pestaña de núcleo o contextual.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Tab, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 410326961df84f6ae62d3c43bee3e651c9533066
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443886"
---
# <a name="tab-element"></a><span data-ttu-id="322f8-104">Tab (Elemento)</span><span class="sxs-lookup"><span data-stu-id="322f8-104">Tab element</span></span>

<span data-ttu-id="322f8-105">Representa una [pestaña de](windowsribbon-controls-tab.md) núcleo [o contextual.](windowsribbon-controls-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="322f8-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="322f8-106">Uso</span><span class="sxs-lookup"><span data-stu-id="322f8-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="322f8-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="322f8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="322f8-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="322f8-108">Attribute</span></span></th>
<th><span data-ttu-id="322f8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="322f8-109">Type</span></span></th>
<th><span data-ttu-id="322f8-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="322f8-110">Required</span></span></th>
<th><span data-ttu-id="322f8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="322f8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="322f8-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="322f8-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="322f8-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="322f8-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="322f8-114">No</span><span class="sxs-lookup"><span data-stu-id="322f8-114">No</span></span><br/></td>
<td><span data-ttu-id="322f8-115">Solo es válido <a href="windowsribbon-element-menugroup.md"><strong>si MenuGroup</strong></a> es el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="322f8-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="322f8-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="322f8-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="322f8-117">Cadena que contiene una lista separada por comas de enteros entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="322f8-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="322f8-118">El espacio en blanco es válido y se omite.</span><span class="sxs-lookup"><span data-stu-id="322f8-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="322f8-119">Longitud máxima: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="322f8-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="322f8-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="322f8-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="322f8-121">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="322f8-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="322f8-122">No</span><span class="sxs-lookup"><span data-stu-id="322f8-122">No</span></span><br/></td>
<td><span data-ttu-id="322f8-123">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="322f8-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="322f8-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="322f8-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="322f8-125">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="322f8-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="322f8-126">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="322f8-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="322f8-127">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="322f8-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="322f8-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="322f8-128">Child elements</span></span>



| <span data-ttu-id="322f8-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="322f8-129">Element</span></span>                                                                         | <span data-ttu-id="322f8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="322f8-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="322f8-131">**Group (Grupo)**</span><span class="sxs-lookup"><span data-stu-id="322f8-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="322f8-132">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="322f8-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="322f8-133">**Tab.ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="322f8-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="322f8-134">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="322f8-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="322f8-135">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="322f8-135">Parent elements</span></span>



| <span data-ttu-id="322f8-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="322f8-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="322f8-137">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="322f8-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="322f8-138">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="322f8-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="322f8-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="322f8-139">Remarks</span></span>

<span data-ttu-id="322f8-140">Necesario.</span><span class="sxs-lookup"><span data-stu-id="322f8-140">Required.</span></span>

<span data-ttu-id="322f8-141">Debe producirse al menos una vez para cada [**elemento Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) [**o TabGroup.**](windowsribbon-element-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="322f8-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="322f8-142">**Tab admite** los [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="322f8-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="322f8-143">Si [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) está presente para el elemento **Tab,** se requiere una entrada para cada elemento [**Group**](windowsribbon-element-group.md) y su tamaño ideal en **ScalingPolicy.IdealSizes.**</span><span class="sxs-lookup"><span data-stu-id="322f8-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="322f8-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="322f8-144">Examples</span></span>

<span data-ttu-id="322f8-145">En el ejemplo siguiente se muestra el marcado básico para el **elemento Tab.**</span><span class="sxs-lookup"><span data-stu-id="322f8-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="322f8-146">En esta sección de código se muestran las **declaraciones del** comando Tab para una **pestaña** Inicio.</span><span class="sxs-lookup"><span data-stu-id="322f8-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="322f8-147">En esta sección de código se muestran las **declaraciones de** control Tab.</span><span class="sxs-lookup"><span data-stu-id="322f8-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="322f8-148">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="322f8-148">Element information</span></span>

- <span data-ttu-id="322f8-149">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="322f8-149">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="322f8-150">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="322f8-150">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="322f8-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="322f8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322f8-152">Control Tab</span><span class="sxs-lookup"><span data-stu-id="322f8-152">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="322f8-153">Control Grupo de pestañas</span><span class="sxs-lookup"><span data-stu-id="322f8-153">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="322f8-154">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="322f8-154">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

