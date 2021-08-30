---
title: Windows Biblioteca de controles del marco de opciones
description: Los temas contenidos en esta sección describen el conjunto de controles que se incluyen con el marco Windows ribbon. Los controles enumerados aquí son los objetos de interfaz de usuario de una cinta de opciones que exponen la funcionalidad Command.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065d69e52cee2300041eedd2d440d292a73e1dc46f5084545effc5e470bceee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933355"
---
# <a name="windows-ribbon-framework-control-library"></a>Windows Biblioteca de controles del marco de opciones

Los temas contenidos en esta sección describen el conjunto de controles que se incluyen con el marco Windows ribbon. Los controles enumerados aquí son los objetos de interfaz de usuario de una cinta de opciones que exponen la funcionalidad Command.

-   [Introducción](#introduction)
-   [Los controles](#windows-ribbon-framework-control-library)
    -   [Controles básicos](#basic-controls)
    -   [Controles de contenedor](#container-controls)
    -   [Controles especializados](#specialized-controls)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

El marco de la cinta de opciones se compone de componentes como [pestañas](windowsribbon-controls-tab.md) y la barra de herramientas de acceso [rápido,](windowsribbon-controls-quickaccesstoolbar.md)que funcionan conjuntamente para ofrecer una experiencia de interfaz de usuario enriquecida. Individualmente, estos componentes exponen diferentes tipos de comandos para ofrecer a los clientes una experiencia organizada y predecible en todas las aplicaciones de la cinta de opciones. Por ejemplo, cada pestaña expone comandos relacionados con la creación y la acción en [](windowsribbon-controls-applicationmenu.md) partes específicas del contenido dentro del área de trabajo de la aplicación, mientras que el menú aplicación expone la funcionalidad relacionada con un proyecto completo, como un documento, una imagen o una película completos.

En este tema se proporciona una lista completa de controles de cinta de opciones e incluye una breve descripción de cada control, con vínculos a documentación más detallada cuando esté disponible.

## <a name="the-controls"></a>Los controles

El marco de la cinta de opciones se compone [de dos vistas:](windowsribbon-reference-elements-view.md)la vista [**de cinta**](windowsribbon-element-ribbon.md) de opciones y la [**vista ContextPopup.**](windowsribbon-element-contextpopup.md) Cada vista puede hospedar varios componentes que actúan como contenedores de presentación para todos los controles representados y administrados por el marco.

La [**vista de**](windowsribbon-element-ribbon.md) cinta de opciones hospeda el elemento [**ApplicationMenu,**](windowsribbon-element-applicationmenu.md) el elemento [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) y la barra de comandos de la cinta de opciones, mientras que la [**vista ContextPopup**](windowsribbon-element-contextpopup.md) hospeda un elemento [**ContextMenu,**](windowsribbon-element-contextmenu.md) un [**elemento MiniToolbar**](windowsribbon-element-minitoolbar.md) o ambos.

Cada control de marco se distingue por la funcionalidad asociada a su [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).

### <a name="basic-controls"></a>Controles básicos

Los controles básicos constan de uno o varios botones que se pueden invocar con un solo clic del mouse para realizar una acción sencilla.

> [!Note]  
> Spinner [**es**](windowsribbon-element-spinner.md) una excepción, ya que contiene un control de edición.

 

En la tabla siguiente se enumeran los controles básicos en el marco de la cinta de opciones.



| Control                                                  | Elemento Markup                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Botón](windowsribbon-controls-button.md)              | [**Botón**](windowsribbon-element-button.md)             |
| [Casilla](windowsribbon-controls-checkbox.md)         | [**Casilla**](windowsribbon-element-checkbox.md)         |
| [Botón Ayuda](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [Botón De alternancia](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Controles de contenedor

Los controles de contenedor se componen de grupos de controles, menús, listas o colecciones de elementos y comandos.

El marco distingue entre dos tipos de contenedores, estáticos y dinámicos.

### <a name="static-containers"></a>Contenedores estáticos

Los contenedores estáticos se declaran y rellenan, junto con todos los recursos asociados, en el archivo de marcado de la cinta de opciones. Estos controles no se pueden modificar en tiempo de ejecución.

Entre las ventajas de los controles estáticos se incluyen las siguientes:

-   Creación rápida de prototipos. Los controles estáticos hacen posible crear rápidamente una simulación de cinta de opciones similar a un diseño final de la cinta de opciones que no requiere código complicado.
-   Modificaciones sencillas. La mayoría de los elementos, atributos, recursos y diseños de controles estáticos se pueden modificar en el marcado.
-   Interfaz de usuario coherente. Las aplicaciones bien diseñadas proporcionan una interfaz de usuario coherente y estable que evita cambios en los menús y listas en tiempo de ejecución.

En la tabla siguiente se describen los controles de contenedor estáticos en el marco de la cinta de opciones.



| Control                                                        | Elemento Markup                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Menú de la aplicación](windowsribbon-controls-applicationmenu.md) | [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) |
| [Elemento emergente de contexto](windowsribbon-controls-contextpopup.md)       | [**ContextPopup**](windowsribbon-element-contextpopup.md)       |
| [Botón desplegable](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Grupo](windowsribbon-controls-group.md)                      | [**Group (Grupo)**](windowsribbon-element-group.md)                     |
| [Grupo de menús](windowsribbon-controls-menugroup.md)             | [**MenuGroup**](windowsribbon-element-menugroup.md)             |
| [Botón Dividir](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [Tabulación](windowsribbon-controls-tab.md)                          | [**Pestaña**](windowsribbon-element-tab.md)                         |
| [Grupo de pestañas](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Contenedores dinámicos

Los contenedores dinámicos se declaran en el archivo de marcado de la cinta de opciones. Presentan un grupo de elementos o comandos que se crean o modifican en tiempo de ejecución.

Una subclase de contenedores dinámicos, denominada galerías, se distingue por su implementación de la [**interfaz IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) Esta interfaz permite a un control exponer su elemento o lista de comandos como una colección y admitir actualizaciones en función de la interacción del usuario y las condiciones en tiempo de ejecución. Para obtener más información, [vea Trabajar con galerías](ribbon-controls-galleries.md).

En la tabla siguiente se enumeran los controles de contenedor dinámicos en el marco de la cinta de opciones.



| Control                                                               | Elemento Markup                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [Cuadro combinado](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Galería desplegable](windowsribbon-controls-dropdowngallery.md)       | [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       |
| [Galería en la cinta de opciones](windowsribbon-controls-inribbongallery.md)       | [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       |
| [Barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md) | [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [Elementos recientes](windowsribbon-controls-recentitems.md)                | [**RecentItems**](windowsribbon-element-recentitems.md)               |
| [Galería de botones de división](windowsribbon-controls-splitbuttongallery.md) | [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Controles especializados

El marco de la cinta de opciones contiene una serie de controles especializados para una funcionalidad de interfaz de usuario específica.

En la tabla siguiente se enumeran los controles especializados en el marco de la cinta de opciones.



| Control                                                                  | Elemento Markup                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Lista desplegable Selector de colores](windowsribbon-controls-dropdowncolorpicker.md) | [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [Control de fuentes](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de comandos y controles](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 