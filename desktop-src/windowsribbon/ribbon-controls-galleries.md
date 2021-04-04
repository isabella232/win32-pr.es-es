---
title: Trabajar con galerías
description: El marco de la cinta de opciones de Windows proporciona a los desarrolladores un modelo sólido y coherente para administrar el contenido dinámico en una variedad de controles basados en colecciones.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Cinta de opciones de Windows, galerías
- Cinta de opciones, galerías
- Cinta de Windows, control DropDownGallery
- Cinta de opciones, control DropDownGallery
- Cinta de Windows, control SplitButtonGallery
- Cinta de opciones, control SplitButtonGallery
- Control DropDownGallery
- Control SplitButtonGallery
- galerías de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793072"
---
# <a name="working-with-galleries"></a>Trabajar con galerías

El marco de la cinta de opciones de Windows proporciona a los desarrolladores un modelo sólido y coherente para administrar el contenido dinámico en una variedad de controles basados en colecciones. Al adaptar y volver a configurar la interfaz de usuario de la cinta de opciones, estos controles dinámicos permiten que el marco de trabajo responda a la interacción del usuario en la propia cinta y la aplicación host, y proporciona la flexibilidad necesaria para controlar diversos entornos en tiempo de ejecución.

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

Esta capacidad del marco de cinta para adaptarse dinámicamente a las condiciones de tiempo de ejecución, los requisitos de la aplicación y los datos proporcionados por el usuario final resalta las amplias capacidades de la interfaz de usuario del marco de trabajo y ofrece a los desarrolladores la flexibilidad de satisfacer una amplia gama de necesidades del cliente.

El objetivo de esta guía es describir los controles dinámicos de la Galería admitidos por el marco, explicar sus diferencias, comentar Cuándo y dónde se pueden usar mejor y demostrar cómo se pueden incorporar en una aplicación de cinta.

## <a name="galleries"></a>Galerías

Las galerías son controles de cuadro de lista de forma funcional y gráficamente enriquecidos. La colección de elementos de una galería se puede organizar por categorías, que se muestra en diseños flexibles basados en filas y columnas, representados con imágenes y texto, y en función del tipo de galería, admiten la vista previa en vivo.

Las galerías son funcionalmente distintas de otros controles dinámicos de la cinta de opciones por los siguientes motivos:

-   Las galerías implementan la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) que define los distintos métodos para manipular colecciones de elementos de la galería.
-   Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce directamente en la cinta de opciones, por ejemplo, cuando un usuario agrega un comando a la barra de herramientas de acceso rápido (QAT).
-   Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce indirectamente desde el entorno de tiempo de ejecución, por ejemplo, cuando un controlador de impresora solo admite diseños de página verticales.
-   Las galerías se pueden actualizar en tiempo de ejecución, en función de la actividad que se produce indirectamente en la aplicación host, como cuando un usuario selecciona un elemento en un documento.

El marco de la cinta de opciones expone dos tipos de galerías: galerías de elementos y galerías de comandos.

### <a name="item-galleries"></a>Galerías de elementos

Las galerías de elementos contienen una colección basada en índices de elementos relacionados en la que cada elemento se representa mediante una imagen, una cadena o ambos. El control está enlazado a un controlador de comandos único que se basa en el valor de índice identificado por la propiedad PKEY de la [interfaz de usuario \_ \_ ](windowsribbon-reference-properties-uipkey-selecteditem.md) .

Las galerías de elementos admiten la vista previa en directo, lo que significa que se muestra el resultado de un comando, basado en mouseover o Focus, sin confirmar ni invocar realmente el comando.

> [!IMPORTANT]
> El marco de trabajo no admite galerías de elementos de hospedaje en el menú de la aplicación.

 

### <a name="command-galleries"></a>Galerías de comandos

Las galerías de comandos contienen una colección de elementos distintos que no están indexados. Cada elemento se representa mediante un único control enlazado a un controlador de comandos a través de un identificador de comando. Al igual que los controles independientes, cada elemento de una galería de comandos enruta los eventos de entrada a un controlador de comandos asociado; la galería de comandos no realiza escuchas de eventos.

Las galerías de comandos no admiten la vista previa dinámica.

### <a name="gallery-controls"></a>Controles de la galería

Hay cuatro controles de galería en el marco de la cinta de opciones: [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)y [**ComboBox**](windowsribbon-element-combobox.md). Todo excepto el **cuadro combinado** se puede implementar como una galería de elementos o una galería de comandos.

### <a name="dropdowngallery"></a>DropDownGallery

Un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) es un botón que muestra una lista desplegable que contiene una colección de elementos o comandos mutuamente excluyentes.

En la captura de pantalla siguiente se muestra el control [Galería desplegable](windowsribbon-controls-dropdowngallery.md) de la cinta de opciones de Microsoft Paint para Windows 7.

![captura de pantalla de un control de Galería desplegable en Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

Un [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) es un control compuesto que expone un único elemento o Comando predeterminado de su colección en un botón principal y muestra otros elementos o comandos en una lista desplegable mutuamente excluyente que se muestra cuando se hace clic en un botón secundario.

En la captura de pantalla siguiente se muestra el control [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md) de la cinta en Microsoft Paint para Windows 7.

![captura de pantalla de un control Galería de botones de división en Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

Un [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) es una galería que muestra una colección de elementos o comandos relacionados en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.

En la captura de pantalla siguiente se muestra el control [Galería de cintas en cinta](windowsribbon-controls-inribbongallery.md) de opciones de Microsoft Paint para Windows 7.

![captura de pantalla de un control de la galería de la cinta de opciones en la cinta de opciones de Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

Un cuadro [**combinado**](windowsribbon-element-combobox.md) es un cuadro de lista de una sola columna que contiene una colección de elementos con un control estático o un control de edición y una flecha de lista desplegable. La parte del cuadro de lista del control se muestra cuando el usuario hace clic en la flecha de lista desplegable.

En la captura de pantalla siguiente se muestra un control de [cuadro combinado](windowsribbon-controls-combobox.md) de la cinta de opciones de Windows Live Movie Maker.

![captura de pantalla de un control ComboBox en la cinta de opciones de Microsoft Paint.](images/controls/combobox.png)

Dado que el [**cuadro combinado**](windowsribbon-element-combobox.md) es exclusivamente una galería de elementos, no admite elementos de comando. También es el único control de la galería que no admite un espacio de comandos. (Un espacio de comandos es una colección de comandos que se declaran en el marcado y que se enumeran en la parte inferior de una galería de elementos o de una galería de comandos).

En el ejemplo de código siguiente se muestra el marcado necesario para declarar un espacio de comandos de tres botones en un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).


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

![captura de pantalla de un espacio de comandos de tres botones en un dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Cómo implementar una galería

En esta sección se describen los detalles de implementación de las galerías de la cinta de opciones y se explica cómo incorporarlas en una aplicación de cinta.

### <a name="the-basic-components"></a>Componentes básicos

En esta sección se describe el conjunto de propiedades y métodos que forman la red troncal de contenido dinámico en el marco de la cinta de opciones y permiten agregar, eliminar, actualizar y, de otro modo, manipular el contenido y el diseño visual de las galerías de la cinta en tiempo de ejecución.

### <a name="iuicollection"></a>IUICollection

Las galerías requieren un conjunto básico de métodos para tener acceso a los elementos individuales de sus colecciones y manipularlos.

La interfaz [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) define estos métodos y el marco complementa su funcionalidad con métodos adicionales que se definen en la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . El marco de trabajo implementa **IUICollection** para cada declaración de galería en el marcado de la cinta de opciones.

Si se requiere una funcionalidad adicional que no proporciona la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , un objeto de colección personalizado implementado por la aplicación host y derivado de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) se puede sustituir por la colección de Framework.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Para que una aplicación responda a los cambios de una colección de la galería, debe implementar la interfaz [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) . Las aplicaciones se pueden suscribir a notificaciones desde un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) a través del agente de escucha de eventos [**IUICollectionChangedEvent:: alchanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .

Cuando la aplicación reemplaza la colección de la Galería proporcionada por el marco de trabajo por una colección personalizada, la aplicación debe implementar la interfaz [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) . Si no se implementa [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) , la aplicación no puede notificar a la plataforma los cambios en la colección personalizada que requieren actualizaciones dinámicas en el control de la galería.

En aquellos casos en los que no se implementa [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) , el control de Galería solo se puede actualizar mediante invalidación a través de [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) y [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), o bien mediante una llamada a [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Las aplicaciones deben implementar IUISimplePropertySet para cada elemento o comando de una colección de la galería. Sin embargo, las propiedades que se pueden solicitar con [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) varían.

Los elementos se definen y se enlazan a una galería a través de la clave de la propiedad [ \_ \_ PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) de la interfaz de usuario y exponen las propiedades con un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Las propiedades válidas para los elementos de las galerías de elementos ([**\_ \_ colección COMMANDTYPE de UI**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) se describen en la tabla siguiente.

> [!Note]  
> Algunas propiedades de elemento, como [la \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario, se pueden definir en el marcado. Para obtener más información, consulte la documentación de referencia de [las claves de propiedad](windowsribbon-reference-properties.md) .

 



Control

Propiedades

[**ComboBox**](windowsribbon-element-combobox.md)

[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Interfaz de usuario \_ \_Etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[Interfaz de usuario \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) es una propiedad de la galería de elementos.



 

En la tabla siguiente se describen las propiedades válidas de los elementos de las galerías de comandos ([**\_ \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)de la interfaz de usuario).



| Control                                                                | Propiedades                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Interfaz de usuario \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [Interfaz de usuario \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Interfaz de usuario \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Las categorías se utilizan para organizar elementos y comandos en galerías. Las categorías se definen y se enlazan a una galería a través de la clave de propiedad de la [interfaz de usuario \_ PKEY \_ categorías](windowsribbon-reference-properties-uipkey-categories.md) y exponen las propiedades con un objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) específico de la categoría.

Las categorías no tienen un CommandType y no admiten la interacción del usuario. Por ejemplo, las categorías no se pueden convertir en SelectedItem en una galería de elementos y no están enlazadas a un comando en una galería de comandos. Al igual que otras propiedades de elementos de la galería, las propiedades de categoría como la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md) de la interfaz de usuario y la [interfaz de usuario \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) se pueden recuperar llamando a [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).

> [!IMPORTANT]
> [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) debe devolver la [**colección de interfaz de usuario \_ \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) cuando se solicita la [interfaz de usuario \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) para un elemento que no tiene una categoría asociada.

 

### <a name="declare-the-controls-in-markup"></a>Declarar los controles en el marcado

Las galerías, como todos los controles de la cinta de opciones, se deben declarar en el marcado. Una galería se identifica en el marcado como una galería de elementos o una galería de comandos y se declaran varios detalles de presentación. A diferencia de otros controles, las galerías solo requieren el control base o el contenedor de la colección para que se declaren en el marcado. Las colecciones reales se rellenan en tiempo de ejecución. Cuando se declara una galería en el marcado, el atributo de *tipo* se usa para especificar si la Galería es una galería de elementos de una galería de comandos.

Hay una serie de atributos de diseño opcionales disponibles para cada uno de los controles que se describen aquí. Estos atributos proporcionan preferencias de desarrollador para que el marco de trabajo siga que afectan directamente a cómo se rellena y se muestra un control en una cinta de opciones. Las preferencias aplicables en el marcado están relacionadas con las plantillas de presentación y diseño, y los comportamientos descritos en [Personalización de una cinta a través de las definiciones de tamaño y las directivas de escalado](windowsribbon-templates.md).

Si un control determinado no permite las preferencias de diseño directamente en el marcado o no se especifican las preferencias de diseño, el marco de trabajo define las convenciones de presentación específicas del control en función de la cantidad de espacio en pantalla disponible.

En los siguientes ejemplos se muestra cómo incorporar un conjunto de galerías en una cinta de opciones.

### <a name="command-declarations"></a>Declaraciones de comandos

Los comandos se deben declarar con un atributo *CommandName* que se utiliza para asociar un control o un conjunto de controles con el comando.

Un atributo *CommandID* que se usa para enlazar un comando a un controlador de comandos cuando se compila el marcado también se puede especificar aquí. Si no se proporciona ningún identificador, el marco de trabajo genera uno.


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

Esta sección contiene ejemplos que muestran el marcado de control básico necesario para los distintos tipos de galería. Muestran cómo declarar los controles de la galería y asociarlos con un comando mediante el atributo *CommandName* .

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
> Dado que [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) está diseñado para mostrar un subconjunto de su colección de elementos en la cinta de opciones sin activar un menú desplegable, proporciona una serie de atributos opcionales que rigen su tamaño y diseño de elemento en la inicialización de la cinta. Estos atributos son exclusivos de **InRibbonGallery** y no están disponibles en los demás controles dinámicos.

 


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



En el ejemplo siguiente se muestra una declaración de control para el [**ComboBox**](windowsribbon-element-combobox.md).


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Crear un controlador de comandos

Para cada comando, el marco de la cinta de opciones requiere un controlador de comandos correspondiente en la aplicación host. Los controladores de comandos se implementan mediante la aplicación host de la cinta de opciones y se derivan de la interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .

> [!Note]  
> Se pueden enlazar varios comandos a un solo controlador de comandos.

 

Un controlador de comandos sirve para dos propósitos:

-   [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responde a las solicitudes de actualización de propiedades. Los valores de las propiedades del comando, como la [interfaz de usuario \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md) o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario, se establecen a través de llamadas a [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) o [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responde a los eventos de ejecución. Este método admite los siguientes tres Estados de ejecución especificados por el [**parámetro \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) de la interfaz de usuario.
    -   El estado de ejecución ejecuta, o confirma, los comandos a los que está enlazado el controlador.
    -   El estado de vista previa muestra una vista previa de los comandos a los que está enlazado el controlador. En esencia, se ejecutan los comandos sin confirmar el resultado.
    -   El estado CancelPreview cancela los comandos de vista previa. Esto es necesario para admitir el recorrido a través de un menú o una lista, y la vista previa secuencial y deshacer los resultados según sea necesario.

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

Después de definir un controlador de comandos, el comando debe estar enlazado al controlador.

En el ejemplo siguiente se muestra cómo enlazar un comando de la galería a un controlador de comandos específico. En este caso, los controles [**ComboBox**](windowsribbon-element-combobox.md) y Gallery se enlazan a sus controladores de comandos respectivos.


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

En el ejemplo siguiente se muestra una implementación personalizada de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para las galerías de elementos y de comandos.

La clase CItemProperties de este ejemplo se deriva de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). Además del método necesario [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), la clase CItemProperties implementa un conjunto de funciones auxiliares para la inicialización y el seguimiento de índices.


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

[Crear una aplicación de cinta](windowsribbon-stepbystep.md)
</dt> <dt>

[Descripción de los comandos y los controles](windowsribbon-commandscontrols.md)
</dt> <dt>

[Instrucciones para la experiencia del usuario en cinta](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Ejemplo de la galería](windowsribbon-gallerysample.md)
</dt> </dl>

 

 