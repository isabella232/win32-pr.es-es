---
title: Biblioteca de controles de Windows Ribbon Framework
description: En los temas incluidos en esta sección se describe el conjunto de controles que se incluyen con el marco de la cinta de opciones de Windows. Los controles que se muestran aquí son los objetos de interfaz de usuario de una cinta que exponen la funcionalidad del comando.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676453"
---
# <a name="windows-ribbon-framework-control-library"></a>Biblioteca de controles de Windows Ribbon Framework

En los temas incluidos en esta sección se describe el conjunto de controles que se incluyen con el marco de la cinta de opciones de Windows. Los controles que se muestran aquí son los objetos de interfaz de usuario de una cinta que exponen la funcionalidad del comando.

-   [Introducción](#introduction)
-   [Los controles](#windows-ribbon-framework-control-library)
    -   [Controles básicos](#basic-controls)
    -   [Controles de contenedor](#container-controls)
    -   [Controles especializados](#specialized-controls)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El marco de cinta se compone de componentes como [pestañas](windowsribbon-controls-tab.md) y la [barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md), que funcionan conjuntamente para ofrecer una experiencia de interfaz de usuario enriquecida. De forma individual, estos componentes exponen distintos tipos de comandos para ofrecer a los clientes una experiencia organizada y predecible en todas las aplicaciones de la cinta. Por ejemplo, cada pestaña expone comandos relacionados con la creación y la actuación en partes específicas del contenido dentro del área de trabajo de la aplicación, mientras que el [menú aplicación](windowsribbon-controls-applicationmenu.md) expone la funcionalidad relacionada con un proyecto completo, como un documento, una imagen o una película completos.

En este tema se proporciona una lista completa de los controles de la cinta de opciones e incluye una breve descripción de cada control, con vínculos a documentación más detallada cuando esté disponible.

## <a name="the-controls"></a>Los controles

El marco de cinta se compone de dos [vistas](windowsribbon-reference-elements-view.md): la vista de la [**cinta**](windowsribbon-element-ribbon.md) de opciones y la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) . Cada vista puede hospedar varios componentes que actúan como contenedores de presentación para todos los controles que el marco de trabajo representa y administra.

La vista de [**cinta**](windowsribbon-element-ribbon.md) hospeda el elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , el elemento [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) y la barra de comandos de la cinta mientras la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) hospeda un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) o ambos.

Cada control de marco de trabajo se distingue por la funcionalidad asociada a su [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).

### <a name="basic-controls"></a>Controles básicos

Los controles básicos se componen de uno o varios botones que se pueden invocar mediante un solo clic del mouse para realizar una acción simple.

> [!Note]  
> El control de [**número**](windowsribbon-element-spinner.md) es una excepción, ya que contiene un control de edición.

 

En la tabla siguiente se enumeran los controles básicos en el marco de la cinta de opciones.



| Control                                                  | Elemento de marcado                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Botón](windowsribbon-controls-button.md)              | [**Botón**](windowsribbon-element-button.md)             |
| [Casilla de verificación](windowsribbon-controls-checkbox.md)         | [**CheckBox**](windowsribbon-element-checkbox.md)         |
| [Botón ayuda](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [Botón de alternancia](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Controles de contenedor

Los controles de contenedor se componen de grupos de controles, menús, listas o colecciones de elementos y comandos.

El marco de trabajo distingue entre dos tipos de contenedores, estáticos y dinámicos.

### <a name="static-containers"></a>Contenedores estáticos

Los contenedores estáticos se declaran y rellenan, junto con todos los recursos asociados, en el archivo de marcado de la cinta de opciones. Estos controles no se pueden modificar en tiempo de ejecución.

Entre las ventajas de los controles estáticos se incluyen las siguientes:

-   Prototipos rápidos. Los controles estáticos permiten compilar rápidamente una maqueta de la cinta de opciones similar a un diseño final de la cinta de opciones que no requiere código complicado.
-   Modificaciones sencillas. La mayoría de los elementos, los atributos, los recursos y los diseños de los controles estáticos se pueden modificar en el marcado.
-   Interfaz de usuario coherente. Las aplicaciones bien diseñadas proporcionan una interfaz de usuario coherente y estable que evita los cambios en los menús y listas en tiempo de ejecución.

En la tabla siguiente se describen los controles de contenedor estático en el marco de la cinta de opciones.



| Control                                                        | Elemento de marcado                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Menú de la aplicación](windowsribbon-controls-applicationmenu.md) | [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) |
| [Cuadro emergente de contexto](windowsribbon-controls-contextpopup.md)       | [**ContextPopup**](windowsribbon-element-contextpopup.md)       |
| [Botón desplegable](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Grupo](windowsribbon-controls-group.md)                      | [**Group (Grupo)**](windowsribbon-element-group.md)                     |
| [Grupo de menús](windowsribbon-controls-menugroup.md)             | [**MenuGroup**](windowsribbon-element-menugroup.md)             |
| [Botón de expansión](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [Tabulación](windowsribbon-controls-tab.md)                          | [**Tabulación**](windowsribbon-element-tab.md)                         |
| [Grupo de pestañas](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Contenedores dinámicos

Los contenedores dinámicos se declaran en el archivo de marcado de la cinta. Incluyen un grupo de elementos o comandos que se crean o modifican en tiempo de ejecución.

Una subclase de contenedores dinámicos, denominados galerías, se distingue por su implementación de la interfaz [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . Esta interfaz permite a un control exponer su elemento o lista de comandos como una colección, y admitir actualizaciones basadas en las condiciones de interacción con el usuario y en tiempo de ejecución. Para obtener más información, vea [trabajar con galerías](ribbon-controls-galleries.md).

En la tabla siguiente se enumeran los controles de contenedor dinámico en el marco de la cinta de opciones.



| Control                                                               | Elemento de marcado                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [Cuadro combinado](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Galería desplegable](windowsribbon-controls-dropdowngallery.md)       | [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       |
| [En la galería de la cinta de opciones](windowsribbon-controls-inribbongallery.md)       | [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       |
| [Barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) | [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [Elementos recientes](windowsribbon-controls-recentitems.md)                | [**RecentItems**](windowsribbon-element-recentitems.md)               |
| [Galería de botones de expansión](windowsribbon-controls-splitbuttongallery.md) | [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Controles especializados

El marco de cinta de opciones contiene una serie de controles especializados para la funcionalidad específica de la interfaz de usuario.

En la tabla siguiente se enumeran los controles especializados en el marco de la cinta de opciones.



| Control                                                                  | Elemento de marcado                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Selector de colores desplegables](windowsribbon-controls-dropdowncolorpicker.md) | [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [Control de fuente](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los comandos y los controles](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 