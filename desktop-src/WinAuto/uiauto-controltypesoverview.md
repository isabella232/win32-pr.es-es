---
title: Información general sobre tipos de control de UI Automation
description: Los Automatización de la interfaz de usuario de control de Microsoft son propiedades que sirven como identificadores conocidos que indican el tipo de control que representa un elemento de interfaz de usuario determinado, como un cuadro combinado o un botón.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Automatización de la interfaz de usuario, información general sobre los tipos de control
- Automatización de la interfaz de usuario,UIA_LocalizedControlTypePropertyId propiedad
- tipos de control, acerca de
- tipos de control, requisitos
- tipos de control, requisitos previos
- tipos de control predefinidos
- tipos de control, UIA_LocalizedControlTypePropertyId propiedad
- tipos de control predefinidos
- UIA_LocalizedControlTypePropertyId propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef59d46e8f0ad00d2613bcec43ee914c71c9edbc1c8501cd2a714df2b883f63f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795485"
---
# <a name="ui-automation-control-types-overview"></a>Información general sobre tipos de control de UI Automation

Los Automatización de la interfaz de usuario de control de Microsoft son propiedades que sirven como identificadores conocidos que indican el tipo de control que representa un elemento de interfaz de usuario determinado, como un cuadro combinado o un botón. Las aplicaciones cliente usan el tipo para identificar las funcionalidades de un control y determinar cómo interactuar con él.

Este tema contiene las siguientes secciones:

-   [Requisitos de los tipos de control de la automatización de la interfaz de usuario](#ui-automation-control-type-requisites)
-   [La propiedad LocalizedControlType](#the-localizedcontroltype-property)
-   [Tipos actuales de control de automatización de la interfaz de usuario](#current-ui-automation-control-types)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Requisitos de los tipos de control de la automatización de la interfaz de usuario

Cada Automatización de la interfaz de usuario tipo de control tiene un conjunto de condiciones asociadas. Cuando un proveedor asigna un tipo de control a un control, el proveedor debe asegurarse de que el control cumple todas las condiciones asociadas a ese tipo de control. Entre las condiciones se incluyen las siguientes:

-   Automatización de la interfaz de usuario de control: cada tipo de control tiene un conjunto de patrones de control que el control debe admitir, un conjunto que es opcional y un conjunto que el control no debe admitir.
-   Valores de propiedad de la automatización de la interfaz de usuario: cada tipo de control tiene un conjunto de propiedades que el control debe admitir.
-   Eventos de automatización de la interfaz de usuario: cada tipo de control tiene un conjunto de eventos que el control debe admitir.
-   Estructura de árbol de automatización de la interfaz de usuario: cada tipo de control define el modo en que debe aparecer el control en la estructura de árbol de automatización de la interfaz de usuario.

Cuando un control cumple las condiciones de un tipo de control determinado, el valor de la propiedad [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**IUIAutomationElement::CachedControlType)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)indicará ese tipo de control.

Si el control no cumple las especificaciones de un tipo de control determinado, use [**\_ CustomControlTypeId**](uiauto-controltype-ids.md) de UIA como identificador de tipo de control y describa completamente el control mediante las propiedades y patrones de control pertinentes. También puede establecer la propiedad [**\_ UIA LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) en una cadena que describa mejor el tipo de control.

## <a name="the-localizedcontroltype-property"></a>La propiedad LocalizedControlType

Si usa un tipo de control predefinido para describir el control, use el valor predeterminado de la propiedad [**\_ UIA LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) y permita que Automatización de la interfaz de usuario proporcione una cadena localizada para que los proveedores exponan correctamente. Si no puede usar un tipo de control predefinido para describir el control, establezca la propiedad **\_ UIA LocalizedControlTypePropertyId** en una cadena localizada que describa con precisión el tipo del control. La cadena debe ser concisa, pero lo suficientemente precisa como para que una tecnología de asistencia, como un lector de pantalla, pueda usarla en la interfaz de usuario para informar al usuario del tipo del control.

## <a name="current-ui-automation-control-types"></a>Tipos actuales de control de automatización de la interfaz de usuario

En los temas siguientes se describen Automatización de la interfaz de usuario tipos de control. Para cada tipo de control, la descripción incluye el conjunto de condiciones que debe admitir un control del tipo especificado:

-   Tipo de control AppBar
-   [Tipo de control Button](uiauto-supportbuttoncontroltype.md)
-   [Tipo de control Calendar](uiauto-supportcalendarcontroltype.md)
-   [Tipo de control CheckBox](uiauto-supportcheckboxcontroltype.md)
-   [Tipo de control ComboBox](uiauto-supportcomboboxcontroltype.md)
-   [Tipo de control DataGrid](uiauto-supportdatagridcontroltype.md)
-   [Tipo de control DataItem](uiauto-supportdataitemcontroltype.md)
-   [Tipo de control De documento](uiauto-supportdocumentcontroltype.md)
-   [Editar tipo de control](uiauto-supporteditcontroltype.md)
-   [Tipo de control Group](uiauto-supportgroupcontroltype.md)
-   [Tipo de control De encabezado](uiauto-supportheadercontroltype.md)
-   [Tipo de control HeaderItem](uiauto-supportheaderitemcontroltype.md)
-   [Tipo de control Hyperlink](uiauto-supporthyperlinkcontroltype.md)
-   [Tipo de control image](uiauto-supportimagecontroltype.md)
-   [Tipo de control List](uiauto-supportlistcontroltype.md)
-   [Tipo de control ListItem](uiauto-supportlistitemcontroltype.md)
-   [Tipo de control menu](uiauto-supportmenucontroltype.md)
-   [Tipo de control MenuBar](uiauto-supportmenubarcontroltype.md)
-   [MenuItem (tipo de control)](uiauto-supportmenuitemcontroltype.md)
-   [Tipo de control Panel](uiauto-supportpanecontroltype.md)
-   [Tipo de control ProgressBar](uiauto-supportprogressbarcontroltype.md)
-   [Tipo de control RadioButton](uiauto-supportradiobuttoncontroltype.md)
-   [Tipo de control ScrollBar](uiauto-supportscrollbarcontroltype.md)
-   [Tipo de control SemanticZoom](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Tipo de control Separador](uiauto-supportseparatorcontroltype.md)
-   [Tipo de control deslizante](uiauto-supportslidercontroltype.md)
-   [Tipo de control Spinner](uiauto-supportspinnercontroltype.md)
-   [Tipo de control SplitButton](uiauto-supportsplitbuttoncontroltype.md)
-   [Tipo de control StatusBar](uiauto-supportstatusbarcontroltype.md)
-   [Tipo de control Tab](uiauto-supporttabcontroltype.md)
-   [Tipo de control TabItem](uiauto-supporttabitemcontroltype.md)
-   [Tipo de control Table](uiauto-supporttablecontroltype.md)
-   [Tipo de control Text](uiauto-supporttextcontroltype.md)
-   [Tipo de control Thumb](uiauto-supportthumbcontroltype.md)
-   [Tipo de control TitleBar](uiauto-supporttitlebarcontroltype.md)
-   [Tipo de control ToolBar](uiauto-supporttoolbarcontroltype.md)
-   [Tipo de control ToolTip](uiauto-supporttooltipcontroltype.md)
-   [Tipo de control Tree](uiauto-supporttreecontroltype.md)
-   [Tipo de control TreeItem](uiauto-supporttreeitemcontroltype.md)
-   [Tipo de control De ventana](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Identificadores de tipo de control](uiauto-controltype-ids.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Compatibilidad con Automatización de la interfaz de usuario de control](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Compatibilidad de UI Automation con controles estándar](uiauto-controlsupport.md)
</dt> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 