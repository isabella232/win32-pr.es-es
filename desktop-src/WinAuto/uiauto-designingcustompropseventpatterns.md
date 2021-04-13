---
title: Diseño de propiedades, eventos y patrones de control personalizados
description: El diseño de una propiedad personalizada, un evento o un patrón de control debe ser útil en una amplia variedad de implementaciones de control.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Automatización de la interfaz de usuario, propiedades personalizadas
- Automatización de la interfaz de usuario, información general sobre eventos
- UI Automation, información general sobre los patrones de control
- Automatización de la interfaz de usuario, diseñar propiedades personalizadas
- Automatización de la interfaz de usuario, diseñar eventos
- Automatización de la interfaz de usuario, diseñar patrones de control
- Automatización de la interfaz de usuario, WinEvents
- propiedades personalizadas, diseñar
- eventos, diseñar
- eventos, WinEvents
- patrones de control, diseñar
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6973356fe6be922e73eef70e5107b6dcabe0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420772"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Diseño de propiedades, eventos y patrones de control personalizados

El diseño de una propiedad personalizada, un evento o un patrón de control debe ser útil en una amplia variedad de implementaciones de control. Los diseños específicos de la aplicación o de control que solo son útiles en escenarios limitados deben evitarse. El diseño debe seguir el ejemplo de las propiedades, los eventos y los patrones de control existentes de la automatización de la interfaz de usuario de Microsoft, que se especificaron cuidadosamente para satisfacer las necesidades de una amplia variedad de aplicaciones de accesibilidad y pruebas automatizadas.

La implementación de la especificación de una propiedad personalizada, evento o patrón de control implica la cooperación y el acuerdo de entidades en los lados del cliente y del proveedor, y requiere que ambas partes implementen la especificación de forma coherente. Se anima a las empresas a trabajar con organizaciones del sector como la [Alianza de interoperabilidad de accesibilidad (AIA)](https://www.atia.org/) para diseñar y publicar la especificación para la propiedad personalizada, el evento o el patrón de control. De esta manera, se puede alcanzar el consenso y se puede garantizar la interoperabilidad con la amplia variedad de aplicaciones.

Este tema contiene las siguientes secciones:

-   [Cuándo usar propiedades y eventos personalizados](#when-to-use-custom-properties-and-events)
-   [Diseñar propiedades personalizadas](#designing-custom-properties)
-   [Diseñar eventos personalizados](#designing-custom-events)
    -   [Eventos de automatización de la interfaz de usuario personalizados y WinEvents](#custom-ui-automation-events-and-winevents)
-   [Diseñar patrones de control personalizados](#designing-custom-control-patterns)
-   [Tipos de controles personalizados](#custom-control-types)
-   [Temas relacionados](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Cuándo usar propiedades y eventos personalizados

Antes de crear una propiedad, un evento o un patrón de control personalizado, asegúrese de que la automatización de la interfaz de usuario no proporciona una solución existente. Por ejemplo, no es necesario crear un patrón de control "click" personalizado porque el patrón de control [Invoke](uiauto-implementinginvoke.md) ya describe esa funcionalidad.

Si decide que se necesita una propiedad, un evento o un patrón de control personalizado, asegúrese de que no sea demasiado impreciso o genérico. Por ejemplo, un patrón de control denominado "show" no es útil porque la visibilidad de un control se puede indicar mediante una propiedad Availability en el elemento, como [**UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) o [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).

Antes de implementar una solución personalizada, confirme cuidadosamente que es necesaria y, a continuación, diseñe la funcionalidad por completo.

## <a name="designing-custom-properties"></a>Diseñar propiedades personalizadas

La automatización de la interfaz de usuario incluye dos tipos básicos de propiedades: las propiedades de los elementos de automatización y las propiedades del patrón de control. Las propiedades del elemento de automatización se componen de un conjunto común de propiedades, como name, AcceleratorKey y ClassName, que exponen todos los elementos de automatización de la interfaz de usuario, independientemente del tipo de control. Un control expone las propiedades de patrón de control a través de un patrón de control determinado. Cada patrón de control tiene un conjunto correspondiente de propiedades de patrón de control que debe exponer el control. Por ejemplo, un control que admite el patrón de control [Grid](uiauto-implementinggrid.md) expone las propiedades ColumnCount y RowCount.

Una propiedad de elemento de automatización personalizada o un patrón de control deben cumplir las siguientes directrices de diseño:

-   Una propiedad personalizada debe tener uno de los siguientes tipos de datos especificados por la enumeración [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . No se admiten otros tipos de datos para las propiedades personalizadas.
    -   **UIAutomationType \_ bool**
    -   **UIAutomationType \_ doble**
    -   **\_Elemento UIAutomationType**
    -   **UIAutomationType \_ int**
    -   **\_Punto UIAutomationType**
    -   **\_Cadena UIAutomationType**
-   Si la propiedad personalizada contiene datos de cadena ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)), la especificación debe indicar si la propiedad es localizable (es decir, si la cadena se puede traducir en distintos idiomas de interfaz de usuario).
-   La propiedad personalizada no debe solaparse con las características o la funcionalidad de las propiedades existentes.

## <a name="designing-custom-events"></a>Diseñar eventos personalizados

Las aplicaciones usan las notificaciones de eventos de UI Automation para responder a los cambios y las acciones que afectan a los elementos de la interfaz de usuario. La mayoría de las propiedades tienen asociados eventos de cambio de propiedad que la automatización de la interfaz de usuario genera cuando cambia el valor de la propiedad. Si introduce una propiedad personalizada, debería considerar la posibilidad de introducir los eventos personalizados correspondientes que también pueden ser necesarios.

Un evento personalizado debe cumplir las siguientes directrices de diseño:

-   El evento personalizado debe ser "sin estado". No se puede asociar a una propiedad o un valor específicos.
-   El evento personalizado no debe superponerse con la definición o el rol de ningún evento existente.

### <a name="custom-ui-automation-events-and-winevents"></a>Eventos de automatización de la interfaz de usuario personalizados y WinEvents

[WinEvents](winevents-infrastructure.md) son un mecanismo de comunicación y eventos de interprocesos útil en la plataforma de Microsoft Windows. Sin embargo, la introducción de un nuevo identificador de WinEvent es arriesgado porque puede provocar colisiones con otras aplicaciones o con el sistema operativo, lo que provoca que el sistema se vuelva inestable. Para evitar colisiones, Microsoft ha definido varias categorías diferentes de WinEvents y, para cada categoría, ha definido uno o más rangos de valores para su uso como ID. de WinEvent. Para obtener más información, consulte [asignación de identificadores de WinEvent](allocation-of-winevent-ids.md).

Los eventos de automatización de la interfaz de usuario personalizados evitan conflictos asignando el identificador de evento internamente en el marco de automatización de la interfaz de usuario.

## <a name="designing-custom-control-patterns"></a>Diseñar patrones de control personalizados

Un patrón de control es una interfaz con propiedades, métodos y eventos que definen una parte de la funcionalidad discreta disponible en un elemento de automatización. Los métodos de patrón de control permiten a los clientes de automatización de la interfaz de usuario manipular un aspecto determinado del control. Las propiedades y los eventos del patrón de control proporcionan información sobre algún aspecto del control y proporcionan información sobre el estado del elemento de automatización que implementa el patrón de control.

Un patrón de control personalizado debe cumplir las siguientes directrices de diseño:

-   Un patrón de control personalizado debe cubrir un escenario determinado. Por ejemplo, el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) está diseñado para consultar un objeto contenido independientemente del estado de virtualización, pero no enumera o cuenta los objetos contenidos.
-   Un patrón de control personalizado no debe superponerse con las características de los patrones de control existentes. Por ejemplo, los patrones de control [Invoke](uiauto-implementinginvoke.md) y [ExpandCollapse](uiauto-implementingexpandcollapse.md) no se deben combinar y presentar como un nuevo patrón de control. Puede reutilizar los patrones de control existentes o definir escenarios únicos con nuevos patrones de control.
-   Varios patrones de control personalizados se pueden diseñar juntos para admitir escenarios complejos. Por ejemplo, los patrones de control [Selection](uiauto-implementingselection.md) y [SelectionItem](uiauto-implementingselectionitem.md) funcionan juntos para admitir escenarios de selección de objetos generales.

## <a name="custom-control-types"></a>Tipos de controles personalizados

Aunque este tema se centra en cómo registrar propiedades, eventos y patrones de control personalizados de la automatización de la interfaz de usuario, también es posible introducir nuevos tipos de control. A diferencia de las propiedades personalizadas, los eventos y los patrones de control, un tipo de control personalizado no se puede registrar mediante programación en tiempo de ejecución porque es realmente simplemente un valor potencial de la propiedad ControlType de automatización de la interfaz de usuario. Sin embargo, un identificador de tipo de control personalizado puede definirse, publicarse y estar disponible para que lo usen otros clientes y proveedores. Para obtener más información sobre los tipos de control, vea [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Registrar propiedades, eventos y patrones de control personalizados](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 