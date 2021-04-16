---
title: Apéndice G Active Accessibility puente a la automatización de la interfaz de usuario
description: Este apéndice contiene información sobre Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5fdc1ebc4d6e17781e383463974f78bb9334aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685532"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Apéndice G: Active Accessibility Bridge a la automatización de la interfaz de usuario

Este apéndice contiene información sobre Microsoft Active Accessibility Bridge. El puente de Active Accessibility permite que las aplicaciones que implementan Microsoft Active Accessibility tengan acceso a las aplicaciones que implementan la automatización de la interfaz de usuario de Microsoft. Mediante el puente entre Microsoft Active Accessibility y la automatización de la interfaz de usuario, los clientes basados en Active Accessibility de Microsoft, como screenreader en Windows XP, pueden interactuar mediante programación con proveedores basados en la automatización de la interfaz de usuario, como una aplicación de Windows Presentation Foundation (WPF). Forma parte de la API principal nativa de automatización de la interfaz de usuario (UIAutomationCore.dll).

El puente de Active Accessibility asigna propiedades y eventos de automatización de la interfaz de usuario a los de Microsoft Active Accessibility. En las tablas siguientes se asignan los métodos y propiedades de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de Microsoft Active Accessibility a la automatización de la interfaz de usuario. Use estas tablas para determinar las prácticas de codificación adecuadas para desarrollar el cliente basado en Microsoft Active Accessibility.

### <a name="navigation-and-hierarchy-properties"></a>Propiedades de navegación y jerarquía



| Propiedad IAccessible                                                     | Propiedad de automatización de la interfaz de usuario          |
|--------------------------------------------------------------------------|---------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | No implementado                 |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Derivado del árbol de automatización de la interfaz de usuario |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Derivado del árbol de automatización de la interfaz de usuario |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | No implementado                 |



 

### <a name="descriptive-properties-and-methods"></a>Propiedades y métodos descriptivos



| IAccessible                                                                          | Automatización de la interfaz de usuario                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Vea los tipos de control y la tabla accRole para obtener más información.                                                                                                                                                                                                                                                                     |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Vea los tipos de control y la tabla accRole para obtener más información.                                                                                                                                                                                                                                                                     |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Si ambos están presentes, AccessKeyProperty tiene prioridad.                                                                                                                                                                                                                         |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. Vea los tipos de control y la tabla accRole para obtener más información.                                                                                                                                                                                                                                                |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Vea los tipos de control y la tabla accRole para obtener más información.                                                                                                                                                                                                                                                                     |
| [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty se admite en tipos de control que admiten el patrón de control [Value](uiauto-implementingvalue.md) o el patrón de control [RangeValue](uiauto-implementingrangevalue.md) . Los valores de RangeValue son coherentes con el comportamiento de Microsoft Active Accessibility (de 0 a 100). Los elementos de valor usan una cadena. |
| [**Put \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty compatible con tipos de control que admiten el patrón de control [Value](uiauto-implementingvalue.md) o el patrón de control [RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | Elemento HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | No implementado                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | No implementado                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Tipos de control y accRole

El rol predeterminado de Microsoft Active Accessibility [**es \_ \_ cliente del sistema de rol**](object-roles.md). Si no se encuentra ninguna acción predeterminada para un tipo de control, el puente de Active Accessibility también usará los siguientes patrones de control disponibles: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)y [Toggle](uiauto-implementingtoggle.md). Por ejemplo, un control GroupBox no tiene ninguna acción predeterminada. Si es compatible con ExpandCollapse, el puente de Active Accessibility lo usará para la acción predeterminada.



| UI Automation (tipo de control)                              | accRole                                                                     | Acción predeterminada                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Botón](uiauto-supportbuttoncontroltype.md)           | [**\_PUSHBUTTON del sistema de roles \_**](object-roles.md)     | Presione                                                    |
| [Calendario](uiauto-supportcalendarcontroltype.md)       | [**\_cliente del sistema de roles \_**](object-roles.md)             | None                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**\_CHECKBUTTON del sistema de roles \_**](object-roles.md)   | Active o desactive (alternancia)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**\_cuadro combinado de sistema de roles \_**](object-roles.md)         | None                                                     |
| Personalizados                                                  | [**\_cliente del sistema de roles \_**](object-roles.md)             | None                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**\_lista de sistema de roles \_**](object-roles.md)                 | None                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**\_ListItem del sistema de roles \_**](object-roles.md)         | None                                                     |
| [Documento](uiauto-supportdocumentcontroltype.md)       | [**\_documento de sistema de roles \_**](object-roles.md)         | None                                                     |
| [Editar](uiauto-supporteditcontroltype.md)               | [**\_texto del sistema de roles \_**](object-roles.md)                 | None                                                     |
| [Grupo](uiauto-supportgroupcontroltype.md)             | [**\_agrupación de sistemas de roles \_**](object-roles.md)         | None                                                     |
| [Header](uiauto-supportheadercontroltype.md)           | [**\_lista de sistema de roles \_**](object-roles.md)                 | None                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**sistema de rol \_ \_ COLUMNHEADER**](object-roles.md) | Haga clic en                                                    |
| [Hipervínculo](uiauto-supporthyperlinkcontroltype.md)     | [**\_vínculo del sistema de roles \_**](object-roles.md)                 | Salto (se asigna a Invoke)                                    |
| [Imagen](uiauto-supportimagecontroltype.md)             | [**\_gráfico del sistema de roles \_**](object-roles.md)           | None                                                     |
| [Lista](uiauto-supportlistcontroltype.md)               | [**\_lista de sistema de roles \_**](object-roles.md)                 | None                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**\_ListItem del sistema de roles \_**](object-roles.md)         | Doble clic                                             |
| [Menú](uiauto-supportmenucontroltype.md)               | [**\_MENUPOPUP del sistema de roles \_**](object-roles.md)       | None                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**\_barra de menús del sistema de roles \_**](object-roles.md)           | None                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**\_MenuItem del sistema de roles \_**](object-roles.md)         | Ejecutar o abrir/cerrar para los elementos de menú que tienen elementos secundarios. |
| [Panel](uiauto-supportpanecontroltype.md)               | [**\_panel del sistema de roles \_**](object-roles.md)                 | None                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**\_PROGRESSBAR del sistema de roles \_**](object-roles.md)   | None                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**\_RADIOBUTTON del sistema de roles \_**](object-roles.md)   | de Azure Functions                                                    |
| [Desplazamiento](uiauto-supportscrollbarcontroltype.md)     | [**\_barra de desplazamiento del sistema de roles \_**](object-roles.md)       | None                                                     |
| [Control deslizante](uiauto-supportslidercontroltype.md)           | [**\_control deslizante del sistema de roles \_**](object-roles.md)             | None                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**\_SPINBUTTON del sistema de roles \_**](object-roles.md)     | None                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**sistema de roles \_ \_ SPLITBUTTON**](object-roles.md)   | None                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**barra de trabajo \_ del sistema de roles \_**](object-roles.md)       | None                                                     |
| [Tabulación](uiauto-supporttabcontroltype.md)                 | [**\_PAGETABLIST del sistema de roles \_**](object-roles.md)   | None                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**\_PAGETAB del sistema de roles \_**](object-roles.md)           | Switch                                                   |
| [Table](uiauto-supporttablecontroltype.md)             | [**\_tabla del sistema de roles \_**](object-roles.md)               | None                                                     |
| [Texto](uiauto-supporttextcontroltype.md)               | [**\_STATICTEXT del sistema de roles \_**](object-roles.md)     | None                                                     |
| [Útil](uiauto-supportthumbcontroltype.md)             | [**\_indicador del sistema de roles \_**](object-roles.md)       | None                                                     |
| [TitleBar](uiauto-supporttitlebarcontroltype.md)       | [**\_TITLEBAR del sistema de roles \_**](object-roles.md)         | None                                                     |
| [Barra](uiauto-supporttoolbarcontroltype.md)         | [**\_barra de herramientas del sistema de roles \_**](object-roles.md)           | None                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**\_ \_ información sobre herramientas del sistema de roles**](object-roles.md)           | None                                                     |
| [Árbol](uiauto-supporttreecontroltype.md)               | [**\_esquema del sistema de roles \_**](object-roles.md)           | None                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**\_OUTLINEITEM del sistema de roles \_**](object-roles.md)   | Expandir o contraer                                       |
| [Ventana](uiauto-supportwindowcontroltype.md)           | [**\_ventana sistema de roles \_**](object-roles.md)             | None                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Propiedades de UI Automation y accState



| accState                                                                                      | Propiedad de automatización de la interfaz de usuario                                                                                                                                                        | Desencadena el cambio de estado |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**sistema de estado \_ \_ activado**](object-state-constants.md)                 | Para ControlType = "CheckBox", use ToggleState. on. Para "RadioButton", use [ **SelectionItemPattern:: IsSelected**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Sí                   |
| [**sistema de estado \_ \_ enfocable**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | No                    |
| [**sistema de estado \_ \_ centrado**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | No                    |
| [**sistema de estado \_ \_ protegido**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | No                    |
| [**\_ReadOnly del sistema de estado \_**](object-state-constants.md)               | IsReadOnlyProperty (patrón de control Value y patrón de control RangeValue)                                                                                                     | No                    |
| [**ESTADO \_ del sistema \_ no disponible**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Sí                   |
| [**sistema de estado \_ \_ vinculado**](object-state-constants.md)                   | ControlTypeProperty = "HYPERLINK"                                                                                                                                             | No                    |
| [**sistema de estado \_ \_ seleccionable**](object-state-constants.md)           | SelectionItemPattern es compatible                                                                                                                                             | No                    |
| [**sistema de estado \_ \_ seleccionado**](object-state-constants.md)               | IsSelectedProperty (patrón de control SelectionItem)                                                                                                                            | No                    |
| [**sistema de estado \_ \_ contraído**](object-state-constants.md)             | ExpandCollapseState = contraído                                                                                                                                               | Sí                   |
| [**sistema de estado \_ \_ expandido**](object-state-constants.md)               | ExpandCollapseState = Expanded o PartiallyExpanded                                                                                                                           | Sí                   |
| [**sistema de estado \_ \_ HASPOPUP**](object-state-constants.md)               | Elementos de menú que admiten expandir o contraer                                                                                                                                       | No                    |
| [**sistema de estado \_ \_ mixto**](object-state-constants.md)                     | ToggleState = indeterminado                                                                                                                                                   | No                    |
| [**\_considerable sistema de estado \_**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | No                    |
| [**sistema de estado \_ \_ móvil**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | No                    |
| [**\_ \_ selección multiseleccionable del sistema de estado**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | No                    |



 

### <a name="selection-and-focus"></a>Selección y foco



| IAccessible                                                            | Automatización de la interfaz de usuario                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation:: FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Consulte las propiedades de UI Automation y la tabla accSelect SELFLAGs para obtener más información.             |
| [**obtener \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern::GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Propiedades de UI Automation y accSelect SELFLAGs



| accSelect SELFLAGs                                                  | Propiedad de automatización de la interfaz de usuario                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ ninguno**](selflag.md)                       | No disponible                                                                                                                  |
| SELFLAG \_ TAKFOCUS                                                   | [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFLAG \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFLAG \_ ADDSELECTION**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFLAG \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFLAG \_ EXTENDSELECTION**](selflag.md) | No disponible                                                                                                                  |



 

### <a name="spatial-mapping"></a>Asignación espacial



| IAccessible                                                 | Automatización de la interfaz de usuario                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Events



| System-Level constantes de evento                                                             | Automatización de la interfaz de usuario                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_MENUPOPUPSTART del sistema de eventos \_**](event-constants.md)     | [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) (Nota: debe comprobar si se trata de una ventana emergente). |
| [**\_MENUPOPUPEND del sistema de eventos \_**](event-constants.md)         | [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                |
| [**\_MENUSTART del sistema de eventos \_**](event-constants.md)               | [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md)                                          |
| [**\_MENUEND del sistema de eventos \_**](event-constants.md)                   | [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)                                              |
| [**\_sonido del sistema de eventos \_**](event-constants.md)                       |                                                                                                                         |
| [**\_alerta del sistema de eventos \_**](event-constants.md)                       |                                                                                                                         |
| [**\_CAPTURESTART del sistema de eventos \_**](event-constants.md)         |                                                                                                                         |
| [**\_CAPTUREEND del sistema de eventos \_**](event-constants.md)             |                                                                                                                         |
| [**\_DIALOGSTART del sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_DIALOGEND del sistema de eventos \_**](event-constants.md)               |                                                                                                                         |
| [**\_MOVESIZESTART del sistema de eventos \_**](event-constants.md)       |                                                                                                                         |
| [**\_MOVESIZEEND del sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_CONTEXTHELPSTART del sistema de eventos \_**](event-constants.md) |                                                                                                                         |
| [**\_CONTEXTHELPEND del sistema de eventos \_**](event-constants.md)     | No es relevante.                                                                                                            |
| [**\_DRAGDROPSTART del sistema de eventos \_**](event-constants.md)       |                                                                                                                         |
| [**\_DRAGDROPEND del sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_SWITCHSTART del sistema de eventos \_**](event-constants.md)           | No es relevante.                                                                                                            |
| [**\_SWITCHEND del sistema de eventos \_**](event-constants.md)               | No es relevante.                                                                                                            |
| [**\_MINIMIZESTART del sistema de eventos \_**](event-constants.md)       |                                                                                                                         |
| [**\_MINIMIZEEND del sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_primer plano del sistema de eventos \_**](event-constants.md)             |                                                                                                                         |
| [**\_SCROLLINGSTART del sistema de eventos \_**](event-constants.md)     | No disponible                                                                                                           |
| [**\_SCROLLINGEND del sistema de eventos \_**](event-constants.md)         | No disponible                                                                                                           |



 



| Object-Level constantes de evento                                                           | Automatización de la interfaz de usuario                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_foco de objeto de evento \_**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**objeto de evento \_ \_ VALUECHANGE**](event-constants.md)         | ValueProperty (patrón de control Value y patrón de control RangeValue)                   |
| [**\_selección de objeto de evento \_**](event-constants.md)             | ElementSelectedEvent (patrón de control SelectionItem)                                   |
| [**objeto de evento \_ \_ SELECTIONADD**](event-constants.md)       | ElementAddedToSelectionEvent (patrón de control SelectionItem)                           |
| [**objeto de evento \_ \_ SELECTIONREMOVE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**objeto de evento \_ \_ SELECTIONWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         | Consulte propiedades de UI Automation y tabla accState para ver los Estados que desencadenan un cambio de estado. |



 

 

 




