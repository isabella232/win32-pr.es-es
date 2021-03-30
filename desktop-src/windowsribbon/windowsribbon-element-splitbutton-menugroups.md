---
title: Propiedad SplitButton. MenuGroups
description: Representa un contenedor para un conjunto de elementos de menú desplegable en un control de botón de expansión estándar.
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- Propiedad SplitButton. MenuGroups de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802246"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="47029-104">Propiedad SplitButton. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="47029-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="47029-105">Representa un contenedor para un conjunto de elementos de menú desplegable en un control de [botón de expansión](windowsribbon-controls-splitbutton.md) estándar.</span><span class="sxs-lookup"><span data-stu-id="47029-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="47029-106">Uso</span><span class="sxs-lookup"><span data-stu-id="47029-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="47029-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="47029-107">Attributes</span></span>

<span data-ttu-id="47029-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="47029-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="47029-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47029-109">Child elements</span></span>



| <span data-ttu-id="47029-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="47029-110">Element</span></span>                                                         | <span data-ttu-id="47029-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="47029-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="47029-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="47029-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="47029-113">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="47029-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="47029-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="47029-114">Parent elements</span></span>



| <span data-ttu-id="47029-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="47029-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="47029-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="47029-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="47029-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47029-117">Remarks</span></span>

<span data-ttu-id="47029-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="47029-118">Optional.</span></span>

<span data-ttu-id="47029-119">Puede producirse como máximo una vez para cada [**splitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="47029-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47029-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="47029-120">Examples</span></span>

<span data-ttu-id="47029-121">En el ejemplo siguiente se muestra el marcado básico para el [botón de expansión](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="47029-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="47029-122">En esta sección de código se muestran las declaraciones de comandos [**splitButton**](windowsribbon-element-splitbutton.md) y **splitButton. MenuGroups** , con un [**Grupo**](windowsribbon-element-group.md) asociado que funciona como contenedor primario del elemento **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="47029-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="47029-123">En esta sección de código se muestran las declaraciones de control [**splitButton**](windowsribbon-element-splitbutton.md) y **splitButton. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="47029-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="47029-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47029-124">Requirements</span></span>



| <span data-ttu-id="47029-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="47029-125">Requirement</span></span> | <span data-ttu-id="47029-126">Value</span><span class="sxs-lookup"><span data-stu-id="47029-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="47029-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47029-127">Minimum supported client</span></span><br/> | <span data-ttu-id="47029-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="47029-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="47029-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47029-129">Minimum supported server</span></span><br/> | <span data-ttu-id="47029-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="47029-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47029-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="47029-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47029-132">Control de botón de expansión</span><span class="sxs-lookup"><span data-stu-id="47029-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





