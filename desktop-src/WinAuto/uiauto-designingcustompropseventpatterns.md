---
title: Diseño de propiedades personalizadas, eventos y patrones de control
description: El diseño de una propiedad personalizada, un evento o un patrón de control debe ser útil en una amplia variedad de implementaciones de control.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Automatización de la interfaz de usuario,propiedades personalizadas
- Automatización de la interfaz de usuario, información general sobre eventos
- Automatización de la interfaz de usuario, información general sobre los patrones de control
- Automatización de la interfaz de usuario, diseñar propiedades personalizadas
- Automatización de la interfaz de usuario, diseñar eventos
- Automatización de la interfaz de usuario, diseñar patrones de control
- Automatización de la interfaz de usuario,WinEvents
- propiedades personalizadas, diseño
- events,designing
- events,WinEvents
- patrones de control, diseño
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5b95d7daa3570e8b4b9b1d61c7c5f5590c6456d83190195e57af66811f1672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324817"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Diseño de propiedades personalizadas, eventos y patrones de control

El diseño de una propiedad personalizada, un evento o un patrón de control debe ser útil en una amplia variedad de implementaciones de control. Se deben evitar los diseños específicos del control o de la aplicación que solo son útiles en escenarios limitados. El diseño debe seguir el ejemplo de las propiedades, eventos y patrones de control existentes de Microsoft Automatización de la interfaz de usuario, que se especificaron cuidadosamente para satisfacer las necesidades de una amplia variedad de aplicaciones de accesibilidad y pruebas automatizadas.

La implementación de la especificación para un patrón de propiedad, evento o control personalizado implica la cooperación y el acuerdo de las partes en los lados cliente y proveedor, y requiere que ambas partes implementen la especificación de forma coherente. Se anima a las empresas a trabajar con organizaciones del sector como [Accessibility Interoperability Alliance (AIA)](https://www.atia.org/) para diseñar y publicar la especificación de la propiedad personalizada, el evento o el patrón de control. De este modo, se puede alcanzar el consenso y se puede garantizar la interoperabilidad con la variedad más amplia de aplicaciones.

Este tema contiene las siguientes secciones:

-   [Cuándo usar eventos y propiedades personalizadas](#when-to-use-custom-properties-and-events)
-   [Diseño de propiedades personalizadas](#designing-custom-properties)
-   [Diseño de eventos personalizados](#designing-custom-events)
    -   [Eventos Automatización de la interfaz de usuario personalizados y WinEvents](#custom-ui-automation-events-and-winevents)
-   [Diseño de patrones de control personalizados](#designing-custom-control-patterns)
-   [Tipos de control personalizados](#custom-control-types)
-   [Temas relacionados](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Cuándo usar eventos y propiedades personalizadas

Antes de crear una propiedad personalizada, un evento o un patrón de control, asegúrese de que Automatización de la interfaz de usuario no proporciona una solución existente. Por ejemplo, no es necesario crear un patrón de control "Click" personalizado porque el [patrón de](uiauto-implementinginvoke.md) control Invoke ya describe esa funcionalidad.

Si decide que se necesita una propiedad personalizada, un evento o un patrón de control, asegúrese de que no sea demasiado impreciso o genérico. Por ejemplo, un patrón de control denominado "Show" no es útil porque la visibilidad de un control se puede indicar mediante una propiedad de disponibilidad en el elemento , como [**UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) o [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).

Antes de implementar una solución personalizada, confirme cuidadosamente que es necesaria y, a continuación, diseñe la funcionalidad por completo.

## <a name="designing-custom-properties"></a>Diseño de propiedades personalizadas

Automatización de la interfaz de usuario incluye dos tipos básicos de propiedades: propiedades de elementos de automatización y propiedades de patrón de control. Las propiedades del elemento de automatización constan de un conjunto común de propiedades, como Name, AcceleratorKey y ClassName, que se exponen por todos los elementos Automatización de la interfaz de usuario, independientemente del tipo de control. Un control expone las propiedades del patrón de control a través de un patrón de control determinado. Cada patrón de control tiene un conjunto correspondiente de propiedades de patrón de control que el control debe exponer. Por ejemplo, un control que admite el patrón de control [Grid](uiauto-implementinggrid.md) expone las propiedades ColumnCount y RowCount.

Una propiedad de elemento de automatización personalizada o una propiedad de patrón de control deben cumplir las siguientes directrices de diseño:

-   Una propiedad personalizada debe tener uno de los siguientes tipos de datos especificados por la [**enumeración UIAutomationType.**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) No se admiten otros tipos de datos para las propiedades personalizadas.
    -   **UIAutomationType \_ Bool**
    -   **UIAutomationType \_ Double**
    -   **Elemento UIAutomationType \_**
    -   **UIAutomationType \_ Int**
    -   **UIAutomationType \_ Point**
    -   **CADENA UIAutomationType \_**
-   Si la propiedad personalizada contiene datos de cadena [**(BSTR),**](/previous-versions/windows/desktop/automat/bstr)la especificación debe especificar si la propiedad es localizable (es decir, si la cadena se puede traducir a distintos idiomas de interfaz de usuario).
-   La propiedad personalizada no debe superponerse con las características o la funcionalidad de las propiedades existentes.

## <a name="designing-custom-events"></a>Diseño de eventos personalizados

Las aplicaciones usan Automatización de la interfaz de usuario notificaciones de eventos para responder a cambios y acciones que implican elementos de interfaz de usuario. La mayoría de las propiedades tienen eventos de cambio de propiedad asociados que Automatización de la interfaz de usuario genera cuando cambia el valor de la propiedad. Si introduce una propiedad personalizada, debe considerar la posibilidad de introducir los eventos personalizados correspondientes que también sean necesarios.

Un evento personalizado debe cumplir las siguientes directrices de diseño:

-   El evento personalizado debe ser "sin estado". No se puede asociar a una propiedad o un valor específicos.
-   El evento personalizado no debe superponerse con la definición o el rol de ningún evento existente.

### <a name="custom-ui-automation-events-and-winevents"></a>Eventos Automatización de la interfaz de usuario personalizados y WinEvents

[WinEvents es](winevents-infrastructure.md) un mecanismo útil de comunicación y eventos entre procesos en la plataforma Windows Microsoft. Sin embargo, la introducción de un nuevo identificador de WinEvent es arriesgada, ya que puede provocar colisiones con otras aplicaciones o con el sistema operativo, lo que hace que el sistema se vuelva inestable. Para evitar colisiones, Microsoft ha definido varias categorías diferentes de WinEvents y, para cada categoría, ha definido uno o varios intervalos de valores para su uso como los IDs de WinEvent. Para obtener más información, vea [Asignación de los IDs de WinEvent.](allocation-of-winevent-ids.md)

Los Automatización de la interfaz de usuario personalizados evitan conflictos mediante la asignación interna del identificador de evento en el marco de trabajo de automatización de la interfaz de usuario.

## <a name="designing-custom-control-patterns"></a>Diseño de patrones de control personalizados

Un patrón de control es una interfaz con propiedades, métodos y eventos que definen una parte discreta de la funcionalidad disponible desde un elemento de automatización. Los métodos de patrón de Automatización de la interfaz de usuario permiten a los clientes manipular un aspecto determinado del control. Las propiedades y eventos del patrón de control proporcionan información sobre algún aspecto del control y proporcionan información sobre el estado del elemento de automatización que implementa el patrón de control.

Un patrón de control personalizado debe cumplir las siguientes directrices de diseño:

-   Un patrón de control personalizado debe cubrir un escenario determinado. Por ejemplo, el patrón de control [ItemContainer](uiauto-implementingitemcontainer.md) está pensado para consultar un objeto contenido independientemente del estado de virtualización, pero no enumera ni cuenta los objetos contenidos.
-   Un patrón de control personalizado no debe superponerse con las características de los patrones de control existentes. Por ejemplo, los [patrones de](uiauto-implementinginvoke.md) control Invoke y [ExpandCollapse](uiauto-implementingexpandcollapse.md) no deben combinarse y presentarse como un nuevo patrón de control. Reutilice los patrones de control existentes o defina escenarios únicos con nuevos patrones de control.
-   Se pueden diseñar varios patrones de control personalizados juntos para admitir escenarios complejos. Por ejemplo, los [patrones de](uiauto-implementingselection.md) control Selection [y SelectionItem](uiauto-implementingselectionitem.md) funcionan conjuntamente para admitir escenarios generales de selección de objetos.

## <a name="custom-control-types"></a>Tipos de control personalizados

Aunque este tema se centra en cómo registrar propiedades Automatización de la interfaz de usuario, eventos y patrones de control personalizados, también es posible introducir nuevos tipos de control. A diferencia de las propiedades personalizadas, los eventos y los patrones de control, un tipo de control personalizado no se puede registrar mediante programación en tiempo de ejecución porque en realidad es solo un valor potencial de la Automatización de la interfaz de usuario ControlType. Sin embargo, un identificador de tipo de control personalizado se puede definir, publicar y hacer que esté disponible para que otros clientes y proveedores los usen. Para obtener más información sobre los tipos de control, [vea Automatización de la interfaz de usuario información general sobre los tipos de control](uiauto-controltypesoverview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Registrar propiedades, eventos y patrones de control personalizados](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 