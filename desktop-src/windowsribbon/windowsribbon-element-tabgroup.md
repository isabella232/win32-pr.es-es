---
title: Elemento TabGroup
description: Representa un conjunto contextual de controles de ficha.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- TabGroup cinta de opciones de Windows
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fcbe0760c850f37c6a7bf348c38e48aa7cf54ddc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104270381"
---
# <a name="tabgroup-element"></a><span data-ttu-id="26727-104">Elemento TabGroup</span><span class="sxs-lookup"><span data-stu-id="26727-104">TabGroup element</span></span>

<span data-ttu-id="26727-105">Representa un conjunto contextual de controles de [ficha](windowsribbon-controls-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="26727-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="26727-106">Uso</span><span class="sxs-lookup"><span data-stu-id="26727-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="26727-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="26727-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26727-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="26727-108">Attribute</span></span></th>
<th><span data-ttu-id="26727-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="26727-109">Type</span></span></th>
<th><span data-ttu-id="26727-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26727-110">Required</span></span></th>
<th><span data-ttu-id="26727-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="26727-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26727-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="26727-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="26727-113">XS: positiveInteger o XS: String</span><span class="sxs-lookup"><span data-stu-id="26727-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="26727-114">No</span><span class="sxs-lookup"><span data-stu-id="26727-114">No</span></span><br/></td>
<td><span data-ttu-id="26727-115">Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="26727-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="26727-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)</span><span class="sxs-lookup"><span data-stu-id="26727-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="26727-117">Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="26727-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="26727-118">El valor debe ser único en el documento XML de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="26727-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="26727-119">Longitud máxima: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="26727-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="26727-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26727-120">Child elements</span></span>



| <span data-ttu-id="26727-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="26727-121">Element</span></span>                                             | <span data-ttu-id="26727-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="26727-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="26727-123">**Tabulación**</span><span class="sxs-lookup"><span data-stu-id="26727-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="26727-124">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="26727-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="26727-125">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="26727-125">Parent elements</span></span>



| <span data-ttu-id="26727-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="26727-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="26727-127">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="26727-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="26727-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26727-128">Remarks</span></span>

<span data-ttu-id="26727-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="26727-129">Required.</span></span>

<span data-ttu-id="26727-130">Debe producirse al menos una vez para cada elemento [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) .</span><span class="sxs-lookup"><span data-stu-id="26727-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="26727-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="26727-131">Examples</span></span>

<span data-ttu-id="26727-132">En el ejemplo siguiente se muestra el marcado básico para el elemento **TabGroup** .</span><span class="sxs-lookup"><span data-stu-id="26727-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="26727-133">En esta sección de código se muestra una declaración de comando **TabGroup** con dos pestañas contextuales.</span><span class="sxs-lookup"><span data-stu-id="26727-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



<span data-ttu-id="26727-134">En esta sección de código se muestran las declaraciones de control **TabGroup** correspondientes.</span><span class="sxs-lookup"><span data-stu-id="26727-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="element-information"></a><span data-ttu-id="26727-135">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="26727-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="26727-136">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26727-136">Minimum supported system</span></span><br/> | <span data-ttu-id="26727-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26727-137">Windows 7</span></span> |
| <span data-ttu-id="26727-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26727-138">Can be empty</span></span>                        | <span data-ttu-id="26727-139">No</span><span class="sxs-lookup"><span data-stu-id="26727-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="26727-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26727-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26727-141">Control de grupo de pestañas</span><span class="sxs-lookup"><span data-stu-id="26727-141">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="26727-142">Control Tab</span><span class="sxs-lookup"><span data-stu-id="26727-142">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





