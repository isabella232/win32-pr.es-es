---
title: Información general sobre tipos de control de UI Automation
description: Los tipos de control de automatización de la interfaz de usuario de Microsoft son propiedades que sirven como identificadores conocidos que indican el tipo de control que representa un determinado elemento de la interfaz de usuario, como un cuadro combinado o un botón.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Automatización de la interfaz de usuario, información general sobre tipos de control
- UI Automation, UIA_LocalizedControlTypePropertyId propiedad
- tipos de controles, acerca de
- tipos de control, requisitos
- tipos de control, requisitos previos
- tipos de control, predefinidos
- tipos de control, propiedad UIA_LocalizedControlTypePropertyId
- tipos de controles predefinidos
- Propiedad UIA_LocalizedControlTypePropertyId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533208"
---
# <a name="ui-automation-control-types-overview"></a>Información general sobre tipos de control de UI Automation

Los tipos de control de automatización de la interfaz de usuario de Microsoft son propiedades que sirven como identificadores conocidos que indican el tipo de control que representa un determinado elemento de la interfaz de usuario, como un cuadro combinado o un botón. Las aplicaciones cliente utilizan el tipo para identificar las capacidades de un control y para determinar cómo interactuar con él.

Este tema contiene las siguientes secciones:

-   [Requisitos de los tipos de control de la automatización de la interfaz de usuario](#ui-automation-control-type-requisites)
-   [La propiedad LocalizedControlType](#the-localizedcontroltype-property)
-   [Tipos actuales de control de automatización de la interfaz de usuario](#current-ui-automation-control-types)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Requisitos de los tipos de control de la automatización de la interfaz de usuario

Cada tipo de control de automatización de la interfaz de usuario tiene un conjunto de condiciones asociadas a él. Cuando un proveedor asigna un tipo de control a un control, el proveedor debe asegurarse de que el control cumpla todas las condiciones asociadas a ese tipo de control. Entre las condiciones se incluyen las siguientes:

-   Patrones de control de UI Automation: cada tipo de control tiene un conjunto de patrones de control que el control debe admitir, un conjunto que es opcional y un conjunto que el control no debe admitir.
-   Valores de propiedad de la automatización de la interfaz de usuario: cada tipo de control tiene un conjunto de propiedades que el control debe admitir.
-   Eventos de automatización de la interfaz de usuario: cada tipo de control tiene un conjunto de eventos que el control debe admitir.
-   Estructura de árbol de automatización de la interfaz de usuario: cada tipo de control define el modo en que debe aparecer el control en la estructura de árbol de automatización de la interfaz de usuario.

Cuando un control cumple las condiciones de un tipo de control determinado, el valor de la propiedad [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**IUIAutomationElement:: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indicará ese tipo de control.

Si el control no cumple las especificaciones para un tipo de control determinado, use [**UIA \_ CUSTOMCONTROLTYPEID**](uiauto-controltype-ids.md) como identificador de tipo de control y describa por completo el control mediante las propiedades y los patrones de control pertinentes. También puede establecer la propiedad [**\_ LocalizedControlTypePropertyId de UIA**](uiauto-automation-element-propids.md) en una cadena que describa mejor el tipo del control.

## <a name="the-localizedcontroltype-property"></a>La propiedad LocalizedControlType

Si usa un tipo de control predefinido para describir el control, use el valor predeterminado de la [**propiedad \_ LocalizedControlTypePropertyId de UIA**](uiauto-automation-element-propids.md) y permita que la automatización de la interfaz de usuario proporcione una cadena localizada para que los proveedores se expongan correctamente. Si no puede usar un tipo de control predefinido para describir el control, establezca la propiedad **\_ LocalizedControlTypePropertyId de UIA** en una cadena traducida que describa con precisión el tipo de control. La cadena debe ser concisa, pero lo suficiente como para que una tecnología de asistencia, como un lector de pantalla, pueda utilizarla en la interfaz de usuario para informar al usuario del tipo del control.

## <a name="current-ui-automation-control-types"></a>Tipos actuales de control de automatización de la interfaz de usuario

En los temas siguientes se describen los tipos de control de automatización de la interfaz de usuario. Para cada tipo de control, la descripción incluye el conjunto de condiciones que un control del tipo especificado debe admitir:

-   AppBar (tipo de control)
-   [Button (tipo de control)](uiauto-supportbuttoncontroltype.md)
-   [Calendar (tipo de control)](uiauto-supportcalendarcontroltype.md)
-   [CheckBox (tipo de control)](uiauto-supportcheckboxcontroltype.md)
-   [ComboBox (tipo de control)](uiauto-supportcomboboxcontroltype.md)
-   [DataGrid (tipo de control)](uiauto-supportdatagridcontroltype.md)
-   [DataItem (tipo de control)](uiauto-supportdataitemcontroltype.md)
-   [Document (tipo de control)](uiauto-supportdocumentcontroltype.md)
-   [Editar tipo de control](uiauto-supporteditcontroltype.md)
-   [Group (tipo de control)](uiauto-supportgroupcontroltype.md)
-   [Header (tipo de control)](uiauto-supportheadercontroltype.md)
-   [HeaderItem (tipo de control)](uiauto-supportheaderitemcontroltype.md)
-   [HYPERLINK (tipo de control)](uiauto-supporthyperlinkcontroltype.md)
-   [Image (tipo de control)](uiauto-supportimagecontroltype.md)
-   [List (tipo de control)](uiauto-supportlistcontroltype.md)
-   [ListItem (tipo de control)](uiauto-supportlistitemcontroltype.md)
-   [Menu (tipo de control)](uiauto-supportmenucontroltype.md)
-   [MenuBar (tipo de control)](uiauto-supportmenubarcontroltype.md)
-   [MenuItem (tipo de control)](uiauto-supportmenuitemcontroltype.md)
-   [Pane (tipo de control)](uiauto-supportpanecontroltype.md)
-   [ProgressBar (tipo de control)](uiauto-supportprogressbarcontroltype.md)
-   [RadioButton (tipo de control)](uiauto-supportradiobuttoncontroltype.md)
-   [ScrollBar (tipo de control)](uiauto-supportscrollbarcontroltype.md)
-   [SemanticZoom (tipo de control)](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Separator (tipo de control)](uiauto-supportseparatorcontroltype.md)
-   [Slide (tipo de control)](uiauto-supportslidercontroltype.md)
-   [Spinner (tipo de control)](uiauto-supportspinnercontroltype.md)
-   [SplitButton (tipo de control)](uiauto-supportsplitbuttoncontroltype.md)
-   [StatusBar (tipo de control)](uiauto-supportstatusbarcontroltype.md)
-   [Tab (tipo de control)](uiauto-supporttabcontroltype.md)
-   [TabItem (tipo de control)](uiauto-supporttabitemcontroltype.md)
-   [Table (tipo de control)](uiauto-supporttablecontroltype.md)
-   [Text (tipo de control)](uiauto-supporttextcontroltype.md)
-   [Thumb (tipo de control)](uiauto-supportthumbcontroltype.md)
-   [TitleBar (tipo de control)](uiauto-supporttitlebarcontroltype.md)
-   [ToolBar (tipo de control)](uiauto-supporttoolbarcontroltype.md)
-   [ToolTip (tipo de control)](uiauto-supporttooltipcontroltype.md)
-   [Tree (tipo de control)](uiauto-supporttreecontroltype.md)
-   [Tipo de control TreeItem](uiauto-supporttreeitemcontroltype.md)
-   [Window (tipo de control)](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Identificadores de tipo de control](uiauto-controltype-ids.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Compatibilidad con tipos de control de UI Automation](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Compatibilidad de UI Automation con controles estándar](uiauto-controlsupport.md)
</dt> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 