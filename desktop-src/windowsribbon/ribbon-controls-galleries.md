---
title: Trabajar con galerías
description: El marco Windows ribbon proporciona a los desarrolladores un modelo sólido y coherente para administrar contenido dinámico en una variedad de controles basados en colecciones.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows Cinta de opciones, galerías
- Cinta de opciones, galerías
- Windows Control Ribbon,DropDownGallery
- Control Ribbon,DropDownGallery
- Windows Control Ribbon,SplitButtonGallery
- Control Ribbon,SplitButtonGallery
- Control DropDownGallery
- Control SplitButtonGallery
- galerías para Windows cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce142c1159d7a7c4129f402716ed7e394ebb4829f043d7c58dd23221b1479720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933455"
---
# <a name="working-with-galleries"></a>Trabajar con galerías

El marco Windows ribbon proporciona a los desarrolladores un modelo sólido y coherente para administrar contenido dinámico en una variedad de controles basados en colecciones. Al adaptar y volver a configurar la interfaz de usuario de la cinta de opciones, estos controles dinámicos permiten al marco responder a la interacción del usuario tanto en la aplicación host como en la propia cinta de opciones, y proporcionan la flexibilidad para controlar varios entornos en tiempo de ejecución.

-   [Introducción](#introduction)
-   [Galerías](#working-with-galleries)
    -   [Galerías de elementos](#item-galleries)
    -   [Galerías de comandos](#command-galleries)
    -   [Controles de la galería](#working-with-galleries)
-   [Cómo implementar una galería](#how-to-implement-a-gallery)
    -   [Componentes básicos](#the-basic-components)
    -   [Declarar los controles en el marcado](#declare-the-controls-in-markup)
    -   [Crear un controlador de comandos](#create-a-command-handler)
    -   [Enlazar el controlador de comandos](#bind-the-command-handler)
    -   [Inicializar una colección](#initialize-a-collection)
    -   [Controlar eventos de colección](#handle-collection-events)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Esta capacidad del marco de la cinta de opciones para adaptarse dinámicamente a las condiciones en tiempo de ejecución, los requisitos de la aplicación y la entrada del usuario final resalta las completas funcionalidades de la interfaz de usuario del marco y proporciona a los desarrolladores la flexibilidad necesaria para satisfacer una amplia gama de necesidades de los clientes.

El objetivo de esta guía es describir los controles dinámicos de la galería admitidos por el marco, explicar sus diferencias, analizar cuándo y dónde se pueden usar mejor y demostrar cómo se pueden incorporar en una aplicación de cinta de opciones.

## <a name="galleries"></a>Galerías

Las galerías son controles de cuadro de lista enriquecidos funcional y gráficamente. La colección de elementos de una galería se puede organizar por categorías, mostrarse en diseños flexibles basados en columnas y filas, representarse con imágenes y texto y, en función del tipo de galería, admitir la vista previa en vivo.

Las galerías son funcionalmente distintas de otros controles dinámicos de la cinta de opciones por los siguientes motivos:

-   Las galerías implementan la [**interfaz IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) que define los distintos métodos para manipular colecciones de elementos de la galería.
-   Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce directamente en la cinta de opciones, como cuando un usuario agrega un comando a la barra de herramientas de acceso rápido (QAT).
-   Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce indirectamente desde el entorno en tiempo de ejecución, como cuando un controlador de impresora solo admite diseños de páginas verticales.
-   Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce indirectamente en la aplicación host, como cuando un usuario selecciona un elemento de un documento.

El marco de la cinta de opciones expone dos tipos de galerías: galerías de elementos y galerías de comandos.

### <a name="item-galleries"></a>Galerías de elementos

Las galerías de elementos contienen una colección basada en índices de elementos relacionados donde cada elemento se representa mediante una imagen, una cadena o ambos. El control está enlazado a un único controlador Command que se basa en el valor de índice identificado por la [ \_ propiedad PKEY \_ SelectedItem de](windowsribbon-reference-properties-uipkey-selecteditem.md) la interfaz de usuario.

Las galerías de elementos admiten la vista previa en vivo, lo que significa mostrar un resultado de comando, basado en el mouseover o el foco, sin confirmar ni invocar realmente al comando.

> [!IMPORTANT]
> El marco no admite el hospedaje de galerías de elementos en el menú Aplicación.

 

### <a name="command-galleries"></a>Galerías de comandos

Las galerías de comandos contienen una colección de elementos distintos y no indexados. Cada elemento se representa mediante un control único enlazado a un controlador de comandos a través de un identificador de comando. Al igual que los controles independientes, cada elemento de una galería de comandos enruta los eventos de entrada a un controlador de comandos asociado: la propia galería de comandos no escucha eventos.

Las galerías de comandos no admiten la vista previa en vivo.

### <a name="gallery-controls"></a>Controles de la galería

Hay cuatro controles de galería en el marco de la cinta de opciones: [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButtonGallery,**](windowsribbon-element-splitbuttongallery.md) [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)y [**ComboBox**](windowsribbon-element-combobox.md). Todos, excepto **ComboBox,** se pueden implementar como una galería de elementos o una galería de comandos.

### <a name="dropdowngallery"></a>DropDownGallery

[**DropDownGallery es**](windowsribbon-element-dropdowngallery.md) un botón que muestra una lista desplegable que contiene una colección de elementos o comandos mutuamente excluyentes.

En la captura de pantalla siguiente se muestra el [control](windowsribbon-controls-dropdowngallery.md) Galería desplegable de la cinta Microsoft Paint para Windows 7.

![captura de pantalla de un control de galería desplegable en Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) es un control compuesto que expone un único elemento predeterminado o Un comando de su colección en un botón principal y muestra otros elementos o comandos en una lista desplegable mutuamente excluyente que se muestra cuando se hace clic en un botón secundario.

En la siguiente captura de pantalla se muestra el control Galería de [botones de](windowsribbon-controls-splitbuttongallery.md) división de la cinta Microsoft Paint para Windows 7.

![captura de pantalla de un control de galería de botón de división en Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

[**InRibbonGallery es**](windowsribbon-element-inribbongallery.md) una galería que muestra una colección de elementos o comandos relacionados en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.

En la siguiente captura de pantalla se muestra el control [De](windowsribbon-controls-inribbongallery.md) la cinta de opciones en la galería de la cinta Microsoft Paint para Windows 7.

![captura de pantalla de un control de la galería en la cinta de opciones de microsoft paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

ComboBox [**es**](windowsribbon-element-combobox.md) un cuadro de lista de una sola columna que contiene una colección de elementos con un control estático o un control de edición y una flecha desplegable. La parte del cuadro de lista del control se muestra cuando el usuario hace clic en la flecha desplegable.

En la siguiente captura de pantalla se muestra un control [Cuadro combinado de](windowsribbon-controls-combobox.md) cinta Windows Live Movie Maker.

![captura de pantalla de un control combobox en la cinta de microsoft paint.](images/controls/combobox.png)

Dado que [**ComboBox**](windowsribbon-element-combobox.md) es exclusivamente una galería de elementos, no admite elementos Command. También es el único control de la galería que no admite un espacio de comandos. (Un espacio de comandos es una colección de comandos declarados en marcado y enumerados en la parte inferior de una galería de elementos o galería de comandos).

En el ejemplo de código siguiente se muestra el marcado necesario para declarar un espacio de comandos de tres botones [**en una clase DropDownGallery**](windowsribbon-element-dropdowngallery.md).


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



En la captura de pantalla siguiente se muestra el espacio de comandos de tres botones del ejemplo de código anterior.

![captura de pantalla de un espacio de comandos de tres botones en una lista desplegable.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Cómo implementar una galería

En esta sección se de abordan los detalles de implementación de las galerías de la cinta de opciones y se explica cómo incorporarlas en una aplicación de cinta de opciones.

### <a name="the-basic-components"></a>Componentes básicos

En esta sección se describe el conjunto de propiedades y métodos que forman la red troncal del contenido dinámico en el marco de la cinta de opciones y admite la adición, eliminación, actualización y manipulación del contenido y el diseño visual de las galerías de la cinta en tiempo de ejecución.

### <a name="iuicollection"></a>IUICollection

Las galerías requieren un conjunto básico de métodos para acceder a los elementos individuales de sus colecciones y manipularlos.

La [interfaz IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) define estos métodos y el marco complementa su funcionalidad con métodos adicionales definidos en la [**interfaz IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) **IUICollection se** implementa mediante el marco para cada declaración de galería en el marcado de la cinta de opciones.

Si se requiere una funcionalidad adicional que no proporciona la interfaz [**IUICollection,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) un objeto de colección personalizado implementado por la aplicación host y derivado de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) se puede sustituir por la colección de marcos.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Para que una aplicación responda a los cambios en una colección de la galería, debe implementar la [**interfaz IUICollectionChangedEvent.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) Las aplicaciones pueden suscribirse a notificaciones desde un [**objeto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través del agente de escucha de [**eventos IUICollectionChangedEvent::OnChanged.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged)

Cuando la aplicación reemplaza la colección de la galería proporcionada por el marco de trabajo por una colección personalizada, la aplicación debe implementar la [interfaz IConnectionPointContainer.](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) Si [no se implementa IConnectionPointContainer,](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) la aplicación no puede notificar al marco de trabajo los cambios en la colección personalizada que requieren actualizaciones dinámicas en el control de la galería.

En aquellos casos en los que no se implementa [IConnectionPointContainer,](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) el control de galería solo se puede actualizar mediante la invalidación a través de [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) e [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), o llamando a [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Las aplicaciones deben implementar IUISimplePropertySet para cada elemento o comando de una colección de la galería. Sin embargo, las propiedades que se pueden solicitar con [**IUISimplePropertySet::GetValue varían.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)

Los elementos se definen y enlazan a una galería a través de la clave de propiedad [ \_ \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) de PKEY de la interfaz de usuario y exponen las propiedades con [**un objeto IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Las propiedades válidas de los elementos de las galerías de elementos [**(UI \_ COMMANDTYPE \_ COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) se describen en la tabla siguiente.

> [!Note]  
> Algunas propiedades de elemento, como [ui \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), se pueden definir en el marcado. Para más información, consulte la documentación de [referencia de claves](windowsribbon-reference-properties.md) de propiedad.

 



Control

Propiedades

[**ComboBox**](windowsribbon-element-combobox.md)

[Interfaz de usuario \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Interfaz de usuario \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[Interfaz de usuario \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Interfaz de usuario \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[Interfaz de usuario \_ PKEY \_ SelectedItem es](windowsribbon-reference-properties-uipkey-selecteditem.md) una propiedad de la galería de elementos.



 

Las propiedades de elemento válidas para las galerías de comandos [**(UI \_ COMMANDTYPE \_ COMMANDCOLLECTION)**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)se describen en la tabla siguiente.



| Control                                                                | Propiedades                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Interfaz de usuario \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [Interfaz de usuario \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Interfaz de usuario \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Las categorías se usan para organizar elementos y comandos en galerías. Las categorías se definen y enlazan a una galería a través de la clave de propiedad Categorías [ \_ PKEY \_](windowsribbon-reference-properties-uipkey-categories.md) de la interfaz de usuario y exponen propiedades con un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) específico de categoría.

Las categorías no tienen un CommandType y no admiten la interacción del usuario. Por ejemplo, las categorías no pueden convertirse en SelectedItem en una galería de elementos y no están enlazadas a un comando en una galería de comandos. Al igual que otras propiedades de elemento de la galería, las propiedades de categoría como ui [ \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md) y [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) se pueden recuperar llamando a [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).

> [!IMPORTANT]
> [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) debe devolver [**UI \_ COLLECTION \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) cuando se solicita [ui \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) para un elemento que no tiene una categoría asociada.

 

### <a name="declare-the-controls-in-markup"></a>Declarar los controles en el marcado

Las galerías, al igual que todos los controles ribbon, deben declararse en el marcado. Una galería se identifica en el marcado como una galería de elementos o galería de comandos, y se declaran varios detalles de presentación. A diferencia de otros controles, las galerías solo requieren que el control base, o contenedor de la colección, se declare en el marcado. Las colecciones reales se rellenan en tiempo de ejecución. Cuando una galería se declara en marcado, el atributo *Type* se usa para especificar si la galería es una galería de elementos de una galería de comandos.

Hay una serie de atributos de diseño opcionales disponibles para cada uno de los controles que se analizan aquí. Estos atributos proporcionan preferencias del desarrollador para que el marco siga y afectan directamente a cómo se rellena y se muestra un control en una cinta de opciones. Las preferencias aplicables en el marcado están relacionadas con las plantillas de presentación y diseño y los comportamientos que se definieron en Personalización de una cinta a través de definiciones de tamaño y [directivas de escalado.](windowsribbon-templates.md)

Si un control determinado no permite preferencias de diseño directamente en el marcado o no se especifican las preferencias de diseño, el marco define convenciones de visualización específicas del control en función de la cantidad de espacio de pantalla disponible.

En los ejemplos siguientes se muestra cómo incorporar un conjunto de galerías en una cinta de opciones.

### <a name="command-declarations"></a>Declaraciones de comandos

Los comandos se deben declarar con un atributo *CommandName* que se usa para asociar un control o conjunto de controles con el comando .

Aquí también se puede especificar un atributo *CommandId* usado para enlazar un comando a un controlador Command cuando se compila el marcado. Si no se proporciona ningún identificador, el marco genera uno.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>Declaraciones de control

Esta sección contiene ejemplos que muestran el marcado de control básico necesario para los distintos tipos de galería. Muestran cómo declarar los controles de la galería y asociarlos a un comando a través del *atributo CommandName.*

En el ejemplo siguiente se muestra una declaración de control para [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) donde se usa el atributo *Type* para especificar que se trata de una galería de comandos.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



En el ejemplo siguiente se muestra una declaración de control para [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



En el ejemplo siguiente se muestra una declaración de control para [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Dado que [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) está diseñado para mostrar un subconjunto de su colección de elementos en la cinta de opciones sin activar un menú desplegable, proporciona una serie de atributos opcionales que rigen su tamaño y diseño de elementos en la inicialización de la cinta de opciones. Estos atributos son únicos para **InRibbonGallery** y no están disponibles en los demás controles dinámicos.

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



En el ejemplo siguiente se muestra una declaración de control para [**comboBox**](windowsribbon-element-combobox.md).


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Crear un controlador de comandos

Para cada comando, el marco de la cinta de opciones requiere un controlador command correspondiente en la aplicación host. Los controladores de comandos se implementan mediante la aplicación host de la cinta de opciones y se derivan de la [**interfaz IUICommandHandler.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)

> [!Note]  
> Varios comandos se pueden enlazar a un único controlador de comandos.

 

Un controlador de comandos tiene dos propósitos:

-   [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responde a las solicitudes de actualización de propiedades. Los valores de las propiedades Command, como [UI \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) o [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), se establecen a través de llamadas a [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) o [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responde a los eventos de ejecución. Este método admite los tres estados de ejecución siguientes especificados por el [**\_ parámetro EXECUTIONVERB de la interfaz de**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) usuario.
    -   El estado Execute ejecuta o confirma los comandos a los que está enlazado el controlador.
    -   El estado de vista previa muestra una vista previa de los comandos a los que está enlazado el controlador. Básicamente, ejecuta los comandos sin confirmar el resultado.
    -   El estado CancelPreview cancela los comandos en vista previa. Esto es necesario para admitir el recorrido a través de un menú o lista y obtener una vista previa secuencial y deshacer los resultados según sea necesario.

En el ejemplo siguiente se muestra un controlador de comandos de la galería.


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>Enlazar el controlador de comandos

Después de definir un controlador de comandos, el comando debe enlazarse al controlador.

En el ejemplo siguiente se muestra cómo enlazar un comando de la galería a un controlador de comandos específico. En este caso, los controles [**ComboBox**](windowsribbon-element-combobox.md) y gallery están enlazados a sus respectivos controladores Command.


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>Inicializar una colección

En el ejemplo siguiente se muestra una implementación personalizada de [**IUISimplePropertySet para**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) las galerías de elementos y comandos.

La clase CItemProperties de este ejemplo se deriva de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). Además del método necesario [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), la clase CItemProperties implementa un conjunto de funciones auxiliares para la inicialización y el seguimiento de índices.


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>Controlar eventos de colección

En el ejemplo siguiente se muestra una implementación de IUICollectionChangedEvent.


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la colección](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Creación de una aplicación de cinta de opciones](windowsribbon-stepbystep.md)
</dt> <dt>

[Descripción de los comandos y controles](windowsribbon-commandscontrols.md)
</dt> <dt>

[Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta de opciones](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Ejemplo de galería](windowsribbon-gallerysample.md)
</dt> </dl>

 

 