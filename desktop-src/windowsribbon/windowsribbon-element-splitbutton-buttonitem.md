---
title: Propiedad SplitButton. ButtonItem
description: Representa un contenedor para un botón o botón de alternancia que expone el comando predeterminado de un botón de expansión.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Propiedad SplitButton. ButtonItem de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489658"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="3c31f-104">Propiedad SplitButton. ButtonItem</span><span class="sxs-lookup"><span data-stu-id="3c31f-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="3c31f-105">Representa un contenedor para un [botón](windowsribbon-controls-button.md) o [botón de alternancia](windowsribbon-controls-togglebutton.md) que expone el comando predeterminado de un [botón de expansión](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3c31f-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="3c31f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="3c31f-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="3c31f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3c31f-107">Attributes</span></span>

<span data-ttu-id="3c31f-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="3c31f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3c31f-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3c31f-109">Child elements</span></span>



| <span data-ttu-id="3c31f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="3c31f-110">Element</span></span>                                                               | <span data-ttu-id="3c31f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c31f-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3c31f-112">**Botón**</span><span class="sxs-lookup"><span data-stu-id="3c31f-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="3c31f-113">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="3c31f-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3c31f-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3c31f-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="3c31f-115">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="3c31f-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3c31f-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3c31f-116">Parent elements</span></span>



| <span data-ttu-id="3c31f-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="3c31f-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="3c31f-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3c31f-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3c31f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c31f-119">Remarks</span></span>

<span data-ttu-id="3c31f-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3c31f-120">Optional.</span></span>

<span data-ttu-id="3c31f-121">Puede producirse como máximo una vez para cada [**splitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3c31f-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="3c31f-122">Cada **splitButton. ButtonItem** solo puede contener un [**botón**](windowsribbon-element-button.md) o un elemento secundario [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="3c31f-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="3c31f-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c31f-123">Examples</span></span>

<span data-ttu-id="3c31f-124">En el ejemplo siguiente se muestra el marcado básico para el [botón de expansión](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3c31f-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="3c31f-125">En esta sección de código se muestran las declaraciones de comandos [**splitButton**](windowsribbon-element-splitbutton.md) y **splitButton. ButtonItem** , con un [**Grupo**](windowsribbon-element-group.md) asociado que funciona como contenedor primario del elemento **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="3c31f-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="3c31f-126">En esta sección de código se muestran las declaraciones de control [**splitButton**](windowsribbon-element-splitbutton.md) y **splitButton. ButtonItem** .</span><span class="sxs-lookup"><span data-stu-id="3c31f-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3c31f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c31f-127">Requirements</span></span>



| <span data-ttu-id="3c31f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c31f-128">Requirement</span></span> | <span data-ttu-id="3c31f-129">Value</span><span class="sxs-lookup"><span data-stu-id="3c31f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3c31f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c31f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3c31f-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c31f-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3c31f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c31f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3c31f-133">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c31f-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c31f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c31f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c31f-135">Control de botón de expansión</span><span class="sxs-lookup"><span data-stu-id="3c31f-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





