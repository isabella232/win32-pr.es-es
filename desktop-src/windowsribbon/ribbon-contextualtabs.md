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
# <a name="displaying-contextual-tabs"></a>Mostrar pestañas contextuales

En una aplicación de marco de cinta de Windows, una pestaña contextual es un control de [pestaña](windowsribbon-controls-tab.md) oculto que se muestra en la fila de pestañas cuando se selecciona o resalta un objeto en el área de trabajo de la aplicación, como una imagen.

-   [Introducción](#introduction)
-   [Implementar pestañas contextuales](#implementing-contextual-tabs)
    -   [marcado](#markup)
    -   [Código](#code)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

A diferencia de las pestañas principales, que contienen varios comandos comunes que son relevantes independientemente del contexto del área de trabajo, las pestañas contextuales contienen normalmente uno o más comandos que solo son aplicables a un objeto seleccionado o resaltado.

Cuando se selecciona un objeto o se resalta en el área de trabajo de la aplicación, el tipo y el contexto del objeto pueden requerir comandos dispares que no hacen que la organización o el sentido funcional estén en una pestaña contextual. En estos casos, es posible que se requieran varias pestañas contextuales, que están contenidas dentro de un [grupo de pestañas](windowsribbon-controls-tabgroup.md). Por ejemplo, la selección de una imagen contenida en una celda de tabla podría requerir dos pestañas contextuales que exponen la funcionalidad de tabla y de imagen.

> [!Note]  
> Además de varias pestañas contextuales, el marco de la cinta de opciones también admite varios controles de [grupo de pestañas](windowsribbon-controls-tabgroup.md) dentro de una cinta.

 

Al mostrar las pestañas contextuales, el marco de la cinta de opciones aplica un conjunto básico de comportamientos que incluyen:

-   Las pestañas contextuales se colocan en el orden en que se declaran y a la derecha de las pestañas principales en la fila de la pestaña de la cinta.
-   Cuando se cambia el tamaño de la cinta de opciones, se escalan las pestañas y las etiquetas de tabulación se truncan como requiere espacio. Sin embargo, las pestañas contextuales visibles tienen una prioridad de presentación superior en la que se escalan y se truncan en último lugar.
-   La etiqueta de un [grupo de pestañas](windowsribbon-controls-tabgroup.md) se muestra en la barra de título de la aplicación y abarca todas las pestañas contextuales asociadas.
-   Cuando se muestran varios controles de [grupo de pestañas](windowsribbon-controls-tabgroup.md) al mismo tiempo, se asigna uno de los cinco colores únicos al fondo de cada grupo de pestañas de la barra de título de la aplicación. Este color también se usa como color de resaltado para las pestañas contextuales del grupo de pestañas.
-   La asignación de color del [grupo de pestañas](windowsribbon-controls-tabgroup.md) se basa en el orden en que se declaran los elementos del grupo de pestañas en el marcado. El marco de trabajo define los colores y la aplicación no puede especificarlos.
-   Los colores del [grupo de pestañas](windowsribbon-controls-tabgroup.md) definidos por el marco de trabajo se pueden modificar indirectamente a través de las claves de propiedad de [las propiedades del marco](windowsribbon-reference-properties-framework.md) . Para obtener más información, vea [personalizar los colores de la cinta](ribbon-color.md)de opciones.
-   Cuando se muestran más de cinco controles de [grupo de pestañas](windowsribbon-controls-tabgroup.md) en un momento determinado, el marco de trabajo recorre los colores asociados.
-   El número máximo de controles de [ficha](windowsribbon-controls-tab.md) en una cinta de opciones está limitado a 100. Esto incluye las pestañas contextuales, visibles o no.

En la siguiente captura de pantalla se muestra una pestaña contextual de Paint de Windows 7.

![captura de pantalla que muestra un control de pestaña contextual.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a>Implementar pestañas contextuales

En esta sección se describen los detalles de implementación de las pestañas contextuales de la cinta de opciones y se explica cómo incorporarlas en una aplicación de cinta.

### <a name="markup"></a>marcado

En los siguientes ejemplos se muestra el marcado básico de un elemento [**TabGroup**](windowsribbon-element-tabgroup.md) que contiene dos pestañas contextuales.

En esta sección de código se muestran las declaraciones de comandos [**TabGroup**](windowsribbon-element-tabgroup.md) y [Tab](windowsribbon-controls-tab.md) .


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



En esta sección de código se muestran las declaraciones de control necesarias para mostrar dos pestañas contextuales dentro de un [**TabGroup**](windowsribbon-element-tabgroup.md).


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



### <a name="code"></a>Código

[Interfaz de usuario \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) es la clave de propiedad única definida por el marco de trabajo para especificar la visibilidad y el estado de las pestañas contextuales. Cuando se selecciona un objeto en el área de trabajo de la aplicación, se puede asignar a esta propiedad uno de los tres valores de la enumeración [**\_ CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) de la interfaz de usuario que definen si existe una pestaña contextual y, si es así, si se muestra como la pestaña activa.

Una aplicación solicita una actualización de [grupo de pestañas](windowsribbon-controls-tabgroup.md) invalidando y actualizando la propiedad PKEY de la [interfaz de usuario \_ \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) cuando cambia el contexto del área de trabajo.

En las secciones de código siguientes se muestra cómo mostrar una pestaña contextual cuando se selecciona una imagen en un área de trabajo de la aplicación.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones para la experiencia del usuario en cinta](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 