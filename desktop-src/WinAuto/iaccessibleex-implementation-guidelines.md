---
title: Instrucciones de implementación de IAccessibleEx
description: Microsoft UI Automation Core puede recuperar todas las propiedades de Microsoft Active Accessibility para cualquier objeto accesible expuesto por un servidor a través de la interfaz IAccessible.
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82403a51e4848142a26194a98dce3922619b06f4
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103785535"
---
# <a name="iaccessibleex-implementation-guidelines"></a>Instrucciones de implementación de IAccessibleEx

Microsoft UI Automation Core puede recuperar todas las propiedades de Microsoft Active Accessibility para cualquier objeto accesible expuesto por un servidor a través de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Al implementar [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), debe exponer solo los aspectos de la funcionalidad de la interfaz de usuario que, de otro modo, no se pueden exponer a través de las propiedades de Microsoft Active Accessibility existentes. En este tema se identifican las propiedades de automatización de la interfaz de usuario y los patrones de control que representan la funcionalidad de la interfaz de usuario que no tiene ningún homólogo en Microsoft Active Accessibility: son las propiedades y los patrones de control que se pueden exponer en una implementación de **IAccessibleEx** .

Este tema contiene las siguientes secciones:

-   [Propiedades](#properties)
-   [Patrones de control](#control-patterns)
-   [WinEvents para eventos de cambio de propiedad de UI Automation](#winevents-for-ui-automation-property-changed-events)
-   [Temas relacionados](#related-topics)

## <a name="properties"></a>Propiedades

Las siguientes propiedades de automatización de la interfaz de usuario no se superponen con la funcionalidad de Microsoft Active Accessibility. Se pueden usar en una implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   AriaProperties
-   AriaRole
-   AutomationId
-   ClassName
-   ClickablePoint
-   ControllerFor
-   Referencia cultural
-   DescribedBy
-   Flujos
-   FrameworkId
-   IsContentElement
-   IsControlElement
-   IsDataValidForForm
-   IsRequiredForForm
-   ItemStatus
-   ItemType
-   LabeledBy
-   LocalizedControlType
-   Orientación

Aunque las propiedades de automatización de la interfaz de usuario de AcceleratorKey y AccessKey se superponen con la propiedad de Microsoft Active Accessibility accKeyboardShortcut, todavía puede usarlas en una implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para los controles que tienen una clave de acceso y un acelerador. Del mismo modo, la propiedad de automatización de la interfaz de usuario ControlType se superpone con la propiedad accRole de Microsoft Active Accessibility, pero todavía se puede usar en una implementación de **IAccessibleEx** para definir un rol más específico para un control.

Dado que las propiedades de los elementos de automatización de la interfaz de usuario ya están tratadas por las propiedades de Microsoft Active Accessibility, no es necesario usarlas en una implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .



| Propiedad de automatización de interfaz de usuario | Equivalente de Microsoft Active Accessibility                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BoundingRectangle      | accLocation                                                                                                                                                                   |
| HasKeyboardFocus       | accState, [ **sistema de estado \_ \_ enfocado**](object-state-constants.md)                                                                                       |
| IsEnabled              | accState, [ **sistema de estado \_ \_ no disponible**](object-state-constants.md)                                                                               |
| IsKeyboardFocusable    | accState, [ **sistema de estado \_ \_ enfocable**](object-state-constants.md)                                                                                   |
| IsPassword             | accState, [ **estado \_ del sistema \_ protegido**](object-state-constants.md)                                                                                   |
| HelpText               | accHelp                                                                                                                                                                       |
| Nombre                   | accName                                                                                                                                                                       |
| NativeWindowHandle     | [**WindowFromAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| IsOffscreen            | accState, sistema de estado [**\_ \_ invisible**](object-state-constants.md)sistema de estado / [**\_ \_ oculto**](object-state-constants.md) |
| ProcessId              | Proporcionado por la UI Automation Core                                                                                                                                                |



 

Para cualquier propiedad de automatización de la interfaz de usuario no admitida, la implementación del método [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) debe establecer el parámetro *pRetVal* en VT \_ vacío y devolver S \_ correcto. Devolver [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) puede hacer que el proxy de MSAA-to-UIA Quite la asignación predeterminada de la propiedad correspondiente.

## <a name="control-patterns"></a>Patrones de control

Los siguientes patrones de control de automatización de la interfaz de usuario no se superponen con la funcionalidad de Microsoft Active Accessibility. Se pueden usar en una implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   Acoplar
-   Expandir y contraer
-   Cuadrícula
-   GridItem
-   MultipleView
-   RangeValue
-   Scroll
-   ScrollItem
-   SynchronizedInput
-   Tabla
-   TableItem
-   Transformación

Para los patrones de control RangeValue y Transform, algunos métodos se superponen entre el patrón de control de automatización de la interfaz de usuario y los métodos de Microsoft Active Accessibility. En estos casos, se deben implementar ambos. Por ejemplo, los métodos [**IAccessible:: get \_ AccValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) y [**IAccessible::P ut \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) de Microsoft Active Accessibility deben implementarse, al igual que los métodos de automatización de la interfaz de usuario [**IRangeValueProvider:: Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) y [**IRangeValueProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) . Internamente, una implementación de puede compartir código para ellos. Este requisito para implementar ambos conjuntos evita tener una implementación parcial de una interfaz de patrón a la vez que mantiene la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilizada por los clientes de Microsoft Active Accessibility existentes.

Los siguientes patrones de control de automatización de la interfaz de usuario no son necesarios cuando el control tiene uno de los roles que se describen a continuación; de lo contrario, se deben admitir explícitamente si procede.



| Patrón de control de UI Automation | Rol de Microsoft Active Accessibility                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**Rol \_ de El \_ PUSHBUTTON del sistema**](object-roles.md), el [**sistema de roles \_ \_ MenuItem**](object-roles.md), el [**sistema de rol \_ \_ BUTTONDROPDOWN**](object-roles.md), el sistema de roles [**\_ \_ SPLITBUTTON**](object-roles.md)y cualquier otro rol en el que el valor de la propiedad accDefaultAction no sea **null**. |
| SelectionItemPattern          | [**Rol \_ de System \_ ListItem**](object-roles.md), [ **\_ \_ RADIOBUTTON del sistema de roles**](object-roles.md)                                                                                                                                                                                                                                                 |
| SelectionPattern              | [**\_lista de sistema de roles \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| TogglePattern                 | [**\_CHECKBUTTON del sistema de roles \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**Rol \_ de \_Texto del sistema**](object-roles.md) (cuando no es de solo lectura), [**\_ \_ PROGRESSBAR del sistema de roles**](object-roles.md), [**\_ \_ cuadro combinado de sistema de roles**](object-roles.md)y cualquier otro rol cuando el valor de la propiedad accValue no sea **null**.                                                                            |
| WindowPattern                 | Se admite automáticamente en los **hWnd** de nivel superior de Microsoft Win32.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>WinEvents para eventos de cambio de propiedad de UI Automation

Además de los eventos definidos para [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), también se definen los siguientes identificadores de eventos y se pueden usar con una implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) como eventos de cambio de propiedad para las propiedades de automatización de la interfaz de usuario correspondientes. Usan el mismo mecanismo que los eventos definidos para **IAccessible**. Para obtener más información, vea [WinEvents](winevents-infrastructure.md).



| IDENTIFICADOR de WinEvent para implementaciones de IAccessibleEx                                                                                              | Identificador de WinEvent relacionado de Microsoft Active Accessibility                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UIA \_ AriaPropertiesPropertyId**](uiauto-automation-element-propids.md)                                    | None                                                                                   |
| [**UIA \_ AriaRolePropertyId**](uiauto-automation-element-propids.md)                                                | None                                                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)                                      | None                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                                          | None                                                                                   |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) | [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ FlowsToPropertyId**](uiauto-automation-element-propids.md)                                                  | None                                                                                   |
| [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md)                                                           | None                                                                                   |
| [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md)                                       | None                                                                                   |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md)                                                   | None                                                                                   |
| [**UIA \_ IsDataValidForFormPropertyId**](uiauto-automation-element-propids.md)                            | None                                                                                   |
| [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)                                              | [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                                            | None                                                                                   |
| [**UIA \_ MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md)                     | None                                                                                   |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md)           | None                                                                                   |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)         | [**objeto de evento \_ \_ CONTENTSCROLLED**](event-constants.md) |
| [**UIA \_ ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md)                   | None                                                                                   |
| [**UIA \_ ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md)               | None                                                                                   |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)             | [**objeto de evento \_ \_ CONTENTSCROLLED**](event-constants.md) |
| [**UIA \_ ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md)                       | None                                                                                   |
| [**UIA \_ ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md)                                 | [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         |



 

En el caso de los eventos anteriores que tienen un valor de objeto de evento \_ \_ enumerado después de ellos, y la implementación de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) debe desencadenar este evento además del evento cambiado indicado. Esto permite que el código de cliente de **IAccessibleEx** existente siga funcionando, a la vez que transmite información de eventos más granular a los clientes interesados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[La interfaz IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




