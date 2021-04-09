---
title: Mostrar pestañas contextuales
description: En una aplicación de marco de cinta de Windows, una pestaña contextual es un control de pestaña oculto que se muestra en la fila de pestañas cuando se selecciona o resalta un objeto en el área de trabajo de la aplicación, como una imagen.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Cinta de opciones de Windows, pestañas contextuales
- Cinta, pestañas contextuales
- Mostrar pestañas contextuales de la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791674"
---
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="731c2-106">Mostrar pestañas contextuales</span><span class="sxs-lookup"><span data-stu-id="731c2-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="731c2-107">En una aplicación de marco de cinta de Windows, una pestaña contextual es un control de [pestaña](windowsribbon-controls-tab.md) oculto que se muestra en la fila de pestañas cuando se selecciona o resalta un objeto en el área de trabajo de la aplicación, como una imagen.</span><span class="sxs-lookup"><span data-stu-id="731c2-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="731c2-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="731c2-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="731c2-109">Implementar pestañas contextuales</span><span class="sxs-lookup"><span data-stu-id="731c2-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="731c2-110">marcado</span><span class="sxs-lookup"><span data-stu-id="731c2-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="731c2-111">Código</span><span class="sxs-lookup"><span data-stu-id="731c2-111">Code</span></span>](#code)
-   [<span data-ttu-id="731c2-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="731c2-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="731c2-113">Introducción</span><span class="sxs-lookup"><span data-stu-id="731c2-113">Introduction</span></span>

<span data-ttu-id="731c2-114">A diferencia de las pestañas principales, que contienen varios comandos comunes que son relevantes independientemente del contexto del área de trabajo, las pestañas contextuales contienen normalmente uno o más comandos que solo son aplicables a un objeto seleccionado o resaltado.</span><span class="sxs-lookup"><span data-stu-id="731c2-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="731c2-115">Cuando se selecciona un objeto o se resalta en el área de trabajo de la aplicación, el tipo y el contexto del objeto pueden requerir comandos dispares que no hacen que la organización o el sentido funcional estén en una pestaña contextual. En estos casos, es posible que se requieran varias pestañas contextuales, que están contenidas dentro de un [grupo de pestañas](windowsribbon-controls-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="731c2-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="731c2-116">Por ejemplo, la selección de una imagen contenida en una celda de tabla podría requerir dos pestañas contextuales que exponen la funcionalidad de tabla y de imagen.</span><span class="sxs-lookup"><span data-stu-id="731c2-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="731c2-117">Además de varias pestañas contextuales, el marco de la cinta de opciones también admite varios controles de [grupo de pestañas](windowsribbon-controls-tabgroup.md) dentro de una cinta.</span><span class="sxs-lookup"><span data-stu-id="731c2-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="731c2-118">Al mostrar las pestañas contextuales, el marco de la cinta de opciones aplica un conjunto básico de comportamientos que incluyen:</span><span class="sxs-lookup"><span data-stu-id="731c2-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="731c2-119">Las pestañas contextuales se colocan en el orden en que se declaran y a la derecha de las pestañas principales en la fila de la pestaña de la cinta.</span><span class="sxs-lookup"><span data-stu-id="731c2-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="731c2-120">Cuando se cambia el tamaño de la cinta de opciones, se escalan las pestañas y las etiquetas de tabulación se truncan como requiere espacio.</span><span class="sxs-lookup"><span data-stu-id="731c2-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="731c2-121">Sin embargo, las pestañas contextuales visibles tienen una prioridad de presentación superior en la que se escalan y se truncan en último lugar.</span><span class="sxs-lookup"><span data-stu-id="731c2-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="731c2-122">La etiqueta de un [grupo de pestañas](windowsribbon-controls-tabgroup.md) se muestra en la barra de título de la aplicación y abarca todas las pestañas contextuales asociadas.</span><span class="sxs-lookup"><span data-stu-id="731c2-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="731c2-123">Cuando se muestran varios controles de [grupo de pestañas](windowsribbon-controls-tabgroup.md) al mismo tiempo, se asigna uno de los cinco colores únicos al fondo de cada grupo de pestañas de la barra de título de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="731c2-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="731c2-124">Este color también se usa como color de resaltado para las pestañas contextuales del grupo de pestañas.</span><span class="sxs-lookup"><span data-stu-id="731c2-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="731c2-125">La asignación de color del [grupo de pestañas](windowsribbon-controls-tabgroup.md) se basa en el orden en que se declaran los elementos del grupo de pestañas en el marcado.</span><span class="sxs-lookup"><span data-stu-id="731c2-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="731c2-126">El marco de trabajo define los colores y la aplicación no puede especificarlos.</span><span class="sxs-lookup"><span data-stu-id="731c2-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="731c2-127">Los colores del [grupo de pestañas](windowsribbon-controls-tabgroup.md) definidos por el marco de trabajo se pueden modificar indirectamente a través de las claves de propiedad de [las propiedades del marco](windowsribbon-reference-properties-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="731c2-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="731c2-128">Para obtener más información, vea [personalizar los colores de la cinta](ribbon-color.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="731c2-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="731c2-129">Cuando se muestran más de cinco controles de [grupo de pestañas](windowsribbon-controls-tabgroup.md) en un momento determinado, el marco de trabajo recorre los colores asociados.</span><span class="sxs-lookup"><span data-stu-id="731c2-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="731c2-130">El número máximo de controles de [ficha](windowsribbon-controls-tab.md) en una cinta de opciones está limitado a 100.</span><span class="sxs-lookup"><span data-stu-id="731c2-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="731c2-131">Esto incluye las pestañas contextuales, visibles o no.</span><span class="sxs-lookup"><span data-stu-id="731c2-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="731c2-132">En la siguiente captura de pantalla se muestra una pestaña contextual de Paint de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="731c2-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![captura de pantalla que muestra un control de pestaña contextual.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="731c2-134">Implementar pestañas contextuales</span><span class="sxs-lookup"><span data-stu-id="731c2-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="731c2-135">En esta sección se describen los detalles de implementación de las pestañas contextuales de la cinta de opciones y se explica cómo incorporarlas en una aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="731c2-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="731c2-136">marcado</span><span class="sxs-lookup"><span data-stu-id="731c2-136">Markup</span></span>

<span data-ttu-id="731c2-137">En los siguientes ejemplos se muestra el marcado básico de un elemento [**TabGroup**](windowsribbon-element-tabgroup.md) que contiene dos pestañas contextuales.</span><span class="sxs-lookup"><span data-stu-id="731c2-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="731c2-138">En esta sección de código se muestran las declaraciones de comandos [**TabGroup**](windowsribbon-element-tabgroup.md) y [Tab](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="731c2-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="731c2-139">En esta sección de código se muestran las declaraciones de control necesarias para mostrar dos pestañas contextuales dentro de un [**TabGroup**](windowsribbon-element-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="731c2-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


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



### <a name="code"></a><span data-ttu-id="731c2-140">Código</span><span class="sxs-lookup"><span data-stu-id="731c2-140">Code</span></span>

<span data-ttu-id="731c2-141">[Interfaz de usuario \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) es la clave de propiedad única definida por el marco de trabajo para especificar la visibilidad y el estado de las pestañas contextuales.</span><span class="sxs-lookup"><span data-stu-id="731c2-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="731c2-142">Cuando se selecciona un objeto en el área de trabajo de la aplicación, se puede asignar a esta propiedad uno de los tres valores de la enumeración [**\_ CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) de la interfaz de usuario que definen si existe una pestaña contextual y, si es así, si se muestra como la pestaña activa.</span><span class="sxs-lookup"><span data-stu-id="731c2-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="731c2-143">Una aplicación solicita una actualización de [grupo de pestañas](windowsribbon-controls-tabgroup.md) invalidando y actualizando la propiedad PKEY de la [interfaz de usuario \_ \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) cuando cambia el contexto del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="731c2-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="731c2-144">En las secciones de código siguientes se muestra cómo mostrar una pestaña contextual cuando se selecciona una imagen en un área de trabajo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="731c2-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="731c2-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="731c2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="731c2-146">Instrucciones para la experiencia del usuario en cinta</span><span class="sxs-lookup"><span data-stu-id="731c2-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="731c2-147">Proceso de diseño de la cinta</span><span class="sxs-lookup"><span data-stu-id="731c2-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 