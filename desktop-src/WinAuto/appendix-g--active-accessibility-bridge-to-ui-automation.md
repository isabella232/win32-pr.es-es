---
title: Apéndice G Active Accessibility Puente a Automatización de la interfaz de usuario
description: Este apéndice contiene información sobre Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14991f869706a16c4def8fdaf49ae255e3ddf413eec416cefd1e151ee470cc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052973"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Apéndice G: Active Accessibility Puente a Automatización de la interfaz de usuario

Este apéndice contiene información sobre Microsoft Active Accessibility Bridge. El Active Accessibility Bridge permite que las aplicaciones que implementan Microsoft Active Accessibility accedan a las aplicaciones que implementan Microsoft Automatización de la interfaz de usuario. Al unir Microsoft Active Accessibility y Automatización de la interfaz de usuario, los clientes basados en Microsoft Active Accessibility, como un lector de pantalla en Windows XP, pueden interactuar mediante programación con proveedores basados en Automatización de la interfaz de usuario de Automatización de la interfaz de usuario, como una aplicación de Windows Presentation Foundation (WPF). Forma parte de la API Automatización de la interfaz de usuario Native Core (UIAutomationCore.dll).

El Active Accessibility Bridge asigna Automatización de la interfaz de usuario propiedades y eventos a los de Microsoft Active Accessibility. En las tablas siguientes se asignan Microsoft Active Accessibility y propiedades de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a Automatización de la interfaz de usuario. Use estas tablas para determinar los procedimientos de codificación adecuados para desarrollar el Microsoft Active Accessibility basado en aplicaciones.

### <a name="navigation-and-hierarchy-properties"></a>Propiedades de navegación y jerarquía



| Propiedad IAccessible                                                     | Automatización de la interfaz de usuario propiedad          |
|--------------------------------------------------------------------------|---------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | No implementado                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Derivado de Automatización de la interfaz de usuario árbol |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Derivado de Automatización de la interfaz de usuario árbol |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | No implementado                 |



 

### <a name="descriptive-properties-and-methods"></a>Propiedades y métodos descriptivos



| IAccessible                                                                          | Automatización de la interfaz de usuario                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Consulte la tabla Tipos de control y accRole para obtener más información.                                                                                                                                                                                                                                                                     |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Consulte la tabla Tipos de control y accRole para obtener más información.                                                                                                                                                                                                                                                                     |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Si ambos están presentes, AccessKeyProperty tiene prioridad.                                                                                                                                                                                                                         |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. Consulte la tabla Tipos de control y accRole para obtener más información.                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Consulte la tabla Tipos de control y accRole para obtener más información.                                                                                                                                                                                                                                                                     |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty; se admite en los tipos de control que [admiten el patrón de](uiauto-implementingvalue.md) control Value o el patrón de control [RangeValue.](uiauto-implementingrangevalue.md) Los valores RangeValue son coherentes con Microsoft Active Accessibility comportamiento (de 0 a 100). Los elementos de valor usan una cadena. |
| [**put \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty; se admite en los tipos de control que admiten [el patrón de](uiauto-implementingvalue.md) control Value o el patrón de control [RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | No implementado                                                                                                                                                                                                                                                                                                          |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | No implementado                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Tipos de control y accRole

El Microsoft Active Accessibility predeterminado es [**ROLE \_ SYSTEM \_ CLIENT**](object-roles.md). Si no se encuentra ninguna acción predeterminada para un tipo de control, Active Accessibility Bridge también usará los siguientes patrones de control disponibles: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)y [Toggle](uiauto-implementingtoggle.md). Por ejemplo, un control groupbox no tiene ninguna acción predeterminada. Si admite ExpandCollapse, el Active Accessibility Bridge lo usará para la acción predeterminada.



| Automatización de la interfaz de usuario de control                              | accRole                                                                     | Acción predeterminada                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Botón](uiauto-supportbuttoncontroltype.md)           | [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md)     | Presione                                                    |
| [Calendario](uiauto-supportcalendarcontroltype.md)       | [**CLIENTE \_ DEL SISTEMA DE \_ ROL**](object-roles.md)             | Ninguno                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**ROLE \_ SYSTEM \_ CHECKBUTTON**](object-roles.md)   | Activar o desactivar (alternar)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**CUADRO \_ COMBINADO DEL SISTEMA DE \_ ROLES**](object-roles.md)         | Ninguno                                                     |
| Personalizado                                                  | [**CLIENTE \_ DEL SISTEMA DE \_ ROL**](object-roles.md)             | Ninguno                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**LISTA \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)                 | Ninguno                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)         | Ninguno                                                     |
| [Documento](uiauto-supportdocumentcontroltype.md)       | [**DOCUMENTO \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)         | Ninguno                                                     |
| [Editar](uiauto-supporteditcontroltype.md)               | [**TEXTO \_ DEL SISTEMA DE \_ ROL**](object-roles.md)                 | Ninguno                                                     |
| [Grupo](uiauto-supportgroupcontroltype.md)             | [**AGRUPACIÓN \_ DEL \_ SISTEMA DE ROLES**](object-roles.md)         | Ninguno                                                     |
| [Header](uiauto-supportheadercontroltype.md)           | [**LISTA \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)                 | Ninguno                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**ROLE \_ SYSTEM \_ COLUMNHEADER**](object-roles.md) | Haga clic en                                                    |
| [Hipervínculo](uiauto-supporthyperlinkcontroltype.md)     | [**VÍNCULO \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)                 | Salto (se asigna a Invoke)                                    |
| [Imagen](uiauto-supportimagecontroltype.md)             | [**GRÁFICO \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)           | Ninguno                                                     |
| [Lista](uiauto-supportlistcontroltype.md)               | [**LISTA \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)                 | Ninguno                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)         | Doble clic                                             |
| [Menú](uiauto-supportmenucontroltype.md)               | [**MENÚ \_ SISTEMA \_ DE ROLESPOPUP**](object-roles.md)       | Ninguno                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**BARRA \_ DE \_ MENÚS DEL SISTEMA DE ROLES**](object-roles.md)           | Ninguno                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**MENUITEM \_ DEL \_ SISTEMA DE ROLES**](object-roles.md)         | Ejecute o abra o cierre para los elementos de menú que tienen elementos secundarios. |
| [Panel](uiauto-supportpanecontroltype.md)               | [**PANEL \_ SISTEMA DE \_ ROLES**](object-roles.md)                 | Ninguno                                                     |
| [Progressbar](uiauto-supportprogressbarcontroltype.md) | [**BARRA \_ DE PROGRESO DEL SISTEMA DE \_ ROLES**](object-roles.md)   | Ninguno                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**ROLE \_ SYSTEM \_ RADIOBUTTON**](object-roles.md)   | de Azure Functions                                                    |
| [Scrollbar](uiauto-supportscrollbarcontroltype.md)     | [**BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL**](object-roles.md)       | Ninguno                                                     |
| [Slider](uiauto-supportslidercontroltype.md)           | [**CONTROL DESLIZANTE \_ DEL SISTEMA \_ DE ROLES**](object-roles.md)             | Ninguno                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**BOTÓN \_ \_ SPINBUTTON DEL SISTEMA DE ROL**](object-roles.md)     | Ninguno                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md)   | Ninguno                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**BARRA DE \_ ESTADO DEL SISTEMA DE \_ ROLES**](object-roles.md)       | Ninguno                                                     |
| [Tabulación](uiauto-supporttabcontroltype.md)                 | [**ROLE \_ SYSTEM \_ PAGETABLIST**](object-roles.md)   | Ninguno                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**ROLE \_ SYSTEM \_ PAGETAB**](object-roles.md)           | Switch                                                   |
| [Tabla](uiauto-supporttablecontroltype.md)             | [**TABLA \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)               | Ninguno                                                     |
| [Texto](uiauto-supporttextcontroltype.md)               | [**ROLE \_ SYSTEM \_ STATICTEXT**](object-roles.md)     | Ninguno                                                     |
| [Pulgar](uiauto-supportthumbcontroltype.md)             | [**INDICADOR \_ DEL SISTEMA DE \_ ROL**](object-roles.md)       | Ninguno                                                     |
| [TitleBar](uiauto-supporttitlebarcontroltype.md)       | [**BARRA \_ DE TÍTULO DEL SISTEMA DE \_ ROLES**](object-roles.md)         | Ninguno                                                     |
| [Barra](uiauto-supporttoolbarcontroltype.md)         | [**BARRA DE \_ HERRAMIENTAS DEL SISTEMA DE \_ ROLES**](object-roles.md)           | Ninguno                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**INFORMACIÓN SOBRE \_ HERRAMIENTAS DEL SISTEMA DE \_ ROLES**](object-roles.md)           | Ninguno                                                     |
| [Árbol](uiauto-supporttreecontroltype.md)               | [**ESQUEMA \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)           | Ninguno                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ OUTLINEITEM**](object-roles.md)   | Expandir o contraer                                       |
| [Ventana](uiauto-supportwindowcontroltype.md)           | [**VENTANA \_ SISTEMA DE \_ ROL**](object-roles.md)             | Ninguno                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Automatización de la interfaz de usuario Properties y accState



| accState                                                                                      | Automatización de la interfaz de usuario propiedad                                                                                                                                                        | Desencadenadores de cambio de estado |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**SISTEMA \_ DE ESTADO \_ ACTIVADO**](object-state-constants.md)                 | Para ControlType = "checkbox", use ToggleState.On. Para "radiobutton", use [ **SelectionItemPattern::IsSelected.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Sí                   |
| [**SISTEMA \_ DE ESTADO QUE SE PUEDE \_ CENTRAR**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | No                    |
| [**SISTEMA \_ DE \_ ESTADO CENTRADO**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | No                    |
| [**STATE \_ SYSTEM \_ PROTECTED**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | No                    |
| [**STATE \_ SYSTEM \_ READONLY**](object-state-constants.md)               | IsReadOnlyProperty (patrón de control Value y patrón de control RangeValue)                                                                                                     | No                    |
| [**SISTEMA \_ DE ESTADO NO \_ DISPONIBLE**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Sí                   |
| [**STATE \_ SYSTEM \_ LINKED**](object-state-constants.md)                   | ControlTypeProperty = "hyperlink"                                                                                                                                             | No                    |
| [**SISTEMA \_ DE \_ ESTADO SELECCIONABLE**](object-state-constants.md)           | Se admite SelectionItemPattern                                                                                                                                             | No                    |
| [**SISTEMA \_ DE ESTADO \_ SELECCIONADO**](object-state-constants.md)               | IsSelectedProperty (patrón de control SelectionItem)                                                                                                                            | No                    |
| [**SISTEMA \_ DE \_ ESTADO CONTRAÍDO**](object-state-constants.md)             | ExpandCollapseState = Collapsed                                                                                                                                               | Sí                   |
| [**SISTEMA \_ DE \_ ESTADO EXPANDIDO**](object-state-constants.md)               | ExpandCollapseState = Expanded o PartiallyExpanded                                                                                                                           | Sí                   |
| [**STATE \_ SYSTEM \_ HASPOPUP**](object-state-constants.md)               | Elementos de menú que admiten Expandir o contraer                                                                                                                                       | No                    |
| [**SISTEMA \_ DE \_ ESTADO MIXTO**](object-state-constants.md)                     | ToggleState = Indeterminate                                                                                                                                                   | No                    |
| [**SISTEMA \_ DE ESTADO CON \_ TAMAÑO**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | No                    |
| [**SISTEMA \_ DE ESTADO \_ MOVEABLE**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | No                    |
| [**SISTEMA \_ DE ESTADO \_ MULTISELECCIONABLE**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | No                    |



 

### <a name="selection-and-focus"></a>Selección y enfoque



| IAccessible                                                            | Automatización de la interfaz de usuario                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation::FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Consulte las Automatización de la interfaz de usuario propiedades y accSelect SELFLAG table (Seleccionar tabla SELFLAG) para obtener más información.             |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern::GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Automatización de la interfaz de usuario propiedades y accSelect SELFLAG



| accSelect SELFLAG                                                  | Automatización de la interfaz de usuario propiedad                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFDETERMINA \_ NONE**](selflag.md)                       | No disponible                                                                                                                  |
| \_SELFDETERMINAFOCUS                                                   | [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFENSA \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern::Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFENSA \_ ADDSELECTION**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFENSA \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFENSA \_ EXTENDSELECTION**](selflag.md) | No disponible                                                                                                                  |



 

### <a name="spatial-mapping"></a>Asignación espacial



| IAccessible                                                 | Automatización de la interfaz de usuario                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Eventos



| System-Level constantes de eventos                                                             | Automatización de la interfaz de usuario                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**MENÚ \_ DEL SISTEMA DE \_ EVENTOSPOPUPSTART**](event-constants.md)     | [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) (Nota: Debe comprobar si se trata de una ventana emergente). |
| [**MENÚ \_ DEL SISTEMA DE \_ EVENTOSPOPUPEND**](event-constants.md)         | [**MenuClosedEventId de UIA \_**](uiauto-event-ids.md)                                                |
| [**MENÚ \_ DEL SISTEMA DE \_ EVENTOSIN INICIO**](event-constants.md)               | [**MenuModeStartEventId de UIA \_**](uiauto-event-ids.md)                                          |
| [**MENÚ \_ DEL SISTEMA DE \_ EVENTOSEND**](event-constants.md)                   | [**MenuModeEndEventId de UIA \_**](uiauto-event-ids.md)                                              |
| [**SONIDO \_ DEL SISTEMA DE \_ EVENTOS**](event-constants.md)                       |                                                                                                                         |
| [**ALERTA \_ DEL SISTEMA DE \_ EVENTOS**](event-constants.md)                       |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ CAPTURESTART**](event-constants.md)         |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ CAPTUREEND**](event-constants.md)             |                                                                                                                         |
| [**CUADRO \_ DE DIÁLOGO SISTEMA DE \_ EVENTOSIN INICIO**](event-constants.md)           |                                                                                                                         |
| [**CUADRO \_ DE DIÁLOGO DEL SISTEMA DE \_ EVENTOSEND**](event-constants.md)               |                                                                                                                         |
| [**INICIO \_ DE \_ MOVESIZE DEL SISTEMA DE EVENTOS**](event-constants.md)       |                                                                                                                         |
| [**\_MOVESIZEEND DEL SISTEMA DE \_ EVENTOS**](event-constants.md)           |                                                                                                                         |
| [**\_CONTEXTHELPSTART DEL SISTEMA DE \_ EVENTOS**](event-constants.md) |                                                                                                                         |
| [**CONTEXTO \_ DEL SISTEMA DE \_ EVENTOSHELPEND**](event-constants.md)     | No es relevante.                                                                                                            |
| [**EVENT \_ SYSTEM \_ DRAGDROPSTART**](event-constants.md)       |                                                                                                                         |
| [**\_DRAGDROPEND DEL SISTEMA DE \_ EVENTOS**](event-constants.md)           |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ SWITCHSTART**](event-constants.md)           | No es relevante.                                                                                                            |
| [**SWITCHEND \_ \_ DEL SISTEMA DE EVENTOS**](event-constants.md)               | No es relevante.                                                                                                            |
| [**EVENT \_ SYSTEM \_ MINIMIZESTART**](event-constants.md)       |                                                                                                                         |
| [**MINIMIZEEND \_ DEL \_ SISTEMA DE EVENTOS**](event-constants.md)           |                                                                                                                         |
| [**PRIMER \_ PLANO DEL SISTEMA DE \_ EVENTOS**](event-constants.md)             |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ SCROLLINGSTART**](event-constants.md)     | No disponible                                                                                                           |
| [**EVENT \_ SYSTEM \_ SCROLLINGEND**](event-constants.md)         | No disponible                                                                                                           |



 



| Object-Level constantes de eventos                                                           | Automatización de la interfaz de usuario                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**FOCO DEL \_ OBJETO \_ DE EVENTO**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**EVENT \_ OBJECT \_ VALUECHANGE**](event-constants.md)         | ValueProperty (patrón de control Value y patrón de control RangeValue)                   |
| [**SELECCIÓN DE \_ OBJETOS \_ DE EVENTO**](event-constants.md)             | ElementSelectedEvent (patrón de control SelectionItem)                                   |
| [**SELECCIÓN \_ DE OBJETOS DE \_ EVENTOAGREGUE**](event-constants.md)       | ElementAddedToSelectionEvent (patrón de control SelectionItem)                           |
| [**SELECCIÓN \_ DE OBJETOS DE \_ EVENTOREMOVE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**EVENT \_ OBJECT \_ SELECTIONWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**EVENT \_ OBJECT \_ STATECHANGE**](event-constants.md)         | Consulte Automatización de la interfaz de usuario propiedades y la tabla accState para ver los estados que desencadenan un cambio de estado. |



 

 

 




