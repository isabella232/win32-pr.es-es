---
title: Propiedad Ribbon. ContextualTabs
description: Representa un contenedor para las pestañas contextuales.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Ribbon. ContextualTabs (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801550"
---
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="4a596-104">Propiedad Ribbon. ContextualTabs</span><span class="sxs-lookup"><span data-stu-id="4a596-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="4a596-105">Representa un contenedor para las pestañas contextuales.</span><span class="sxs-lookup"><span data-stu-id="4a596-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="4a596-106">Uso</span><span class="sxs-lookup"><span data-stu-id="4a596-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="4a596-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a596-107">Attributes</span></span>

<span data-ttu-id="4a596-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="4a596-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4a596-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a596-109">Child elements</span></span>



| <span data-ttu-id="4a596-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a596-110">Element</span></span>                                                       | <span data-ttu-id="4a596-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a596-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4a596-112">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="4a596-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="4a596-113">Debe aparecer al menos una vez</span><span class="sxs-lookup"><span data-stu-id="4a596-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4a596-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4a596-114">Parent elements</span></span>



| <span data-ttu-id="4a596-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a596-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="4a596-116">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="4a596-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4a596-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a596-117">Remarks</span></span>

<span data-ttu-id="4a596-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4a596-118">Optional.</span></span>

<span data-ttu-id="4a596-119">Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="4a596-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="4a596-120">Las pestañas contextuales son útiles para mostrar funciones que solo son relevantes para un contexto de aplicación específico, como una pestaña formato de imagen en un editor de texto que solo se muestra cuando se resalta una imagen.</span><span class="sxs-lookup"><span data-stu-id="4a596-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="4a596-121">Normalmente, las pestañas contextuales no son visibles hasta que se produce un contexto de aplicación específico y la aplicación notifica al marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="4a596-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="4a596-122">Cuando se muestra, las pestañas contextuales están codificadas por colores para diferenciarlas de las pestañas normales.</span><span class="sxs-lookup"><span data-stu-id="4a596-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="4a596-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4a596-123">Examples</span></span>

<span data-ttu-id="4a596-124">En el ejemplo siguiente se muestra el marcado básico para el elemento **Ribbon. ContextualTabs** .</span><span class="sxs-lookup"><span data-stu-id="4a596-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="4a596-125">En esta sección de código se muestra una declaración de comandos de [**TabGroup**](windowsribbon-element-tabgroup.md) y dos declaraciones de comandos de [**pestaña**](windowsribbon-element-tab.md) contextuales.</span><span class="sxs-lookup"><span data-stu-id="4a596-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="4a596-126">En esta sección de código se muestra la declaración de control **Ribbon. ContextualTabs** con un [**TabGroup**](windowsribbon-element-tabgroup.md) y dos controles de [**ficha**](windowsribbon-element-tab.md) contextuales.</span><span class="sxs-lookup"><span data-stu-id="4a596-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4a596-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a596-127">Requirements</span></span>



| <span data-ttu-id="4a596-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a596-128">Requirement</span></span> | <span data-ttu-id="4a596-129">Value</span><span class="sxs-lookup"><span data-stu-id="4a596-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a596-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a596-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4a596-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a596-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4a596-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a596-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4a596-133">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a596-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a596-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a596-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a596-135">**Cinta. pestañas**</span><span class="sxs-lookup"><span data-stu-id="4a596-135">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





