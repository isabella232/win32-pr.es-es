---
title: Acerca de los patrones de control Text y TextRange
description: El contenido textual de un control se expone mediante el patrón de control Text, que representa el contenido de un contenedor de texto como una secuencia de texto.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Automatización de la interfaz de usuario, compatibilidad de contenido textual
- UI Automation, información general sobre el patrón de texto
- Automatización de la interfaz de usuario, información general sobre controles de texto
- Automatización de la interfaz de usuario, patrón de control Text
- Automatización de la interfaz de usuario, Text Services Framework (TSF)
- Automatización de la interfaz de usuario, TSF
- Automatización de la interfaz de usuario, rendimiento
- patrones de texto, acerca de
- patrones de texto, Text Services Framework (TSF)
- controles de texto, acerca de
- contenido textual, compatibilidad con
- controles de texto, rendimiento
- Text (patrón de control)
- patrones de control, texto
- Text Services Framework (TSF)
- TSF (marco de trabajo de servicios de texto)
- rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9ff1eb75227454e3e9df6035798a304096a958
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705019"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Acerca de los patrones de control Text y TextRange

El contenido textual de un control se expone mediante el patrón de control [Text](uiauto-implementingtextandtextrange.md) , que representa el contenido de un contenedor de texto como una secuencia de texto. El patrón de control Text requiere la compatibilidad del patrón de control TextRange para exponer los atributos Format y Style. El patrón de control TextRange admite el patrón de control text mediante la representación de intervalos de texto contiguos o varios (o rangos) en un contenedor de texto con una colección de extremos de inicio y fin. El patrón de control TextRange admite funcionalidad como selección, comparación, recuperación y exploración transversal.

> [!Note]  
> El patrón de control [Text](uiauto-implementingtextandtextrange.md) no proporciona un medio para insertar o modificar texto. Sin embargo, dependiendo del control, esto puede realizarse mediante el patrón de control [valor](uiauto-implementingvalue.md) de Microsoft UI Automation o a través de la entrada de teclado directa. También hay un patrón [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) que admite el cambio mediante programación del texto.

 

La funcionalidad descrita en este tema es fundamental para los proveedores de tecnología de asistencia y sus usuarios finales. Las tecnologías de asistencia pueden usar la automatización de la interfaz de usuario para recopilar información de formato de texto completa para el usuario y proporcionar navegación y selección de texto mediante programación por [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (carácter, palabra, línea o párrafo).

Este tema contiene las siguientes secciones:

-   [UI Automation TextPattern y el marco de trabajo de servicios de texto](#ui-automation-textpattern-and-the-text-services-framework)
-   [Tipos de controles](#control-types)
-   [Interfaces de proveedor](#provider-interfaces)
-   [Interfaces de cliente](#client-interfaces)
-   [Rendimiento](#performance)
-   [Patrón de texto y objetos incrustados virtualizados](#text-pattern-and-virtualized-embedded-objects)
-   [Usar el tipo de control personalizado con el patrón de control Text](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Duración de un intervalo de texto](#lifetime-of-a-text-range)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>UI Automation TextPattern y el marco de trabajo de servicios de texto

Text Services Framework (TSF) es un marco de trabajo del sistema simple y escalable que habilita los servicios de lenguaje natural y la entrada de texto avanzada en el escritorio y en las aplicaciones. Además de proporcionar interfaces para que las aplicaciones expongan su almacén de texto, también admite metadatos para el almacén de texto.

TSF se diseñó para aplicaciones que necesitan insertar entradas en escenarios que contengan contexto. Sin embargo, el patrón de control [Text](uiauto-implementingtextandtextrange.md) es una solución de solo lectura diseñada para proporcionar acceso optimizado a un almacén de texto para los lectores de pantalla y dispositivos Braille.

Las tecnologías accesibles que requieren acceso de solo lectura a un almacén de texto pueden usar el patrón de control Text, pero necesitarán la funcionalidad de TSF para la entrada contextual.

Para obtener más información, vea [Text Services Framework](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Tipos de controles

El tipo de control de [edición](uiauto-supporteditcontroltype.md) de automatización de la interfaz de usuario y el tipo de control de [documento](uiauto-supportdocumentcontroltype.md) deben admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) . Para mejorar la accesibilidad, Microsoft recomienda que los tipos de control de texto y la [información sobre herramientas](uiauto-supporttooltipcontroltype.md) también admitan el patrón de control Text, pero no es obligatorio.

## <a name="provider-interfaces"></a>Interfaces de proveedor

Los proveedores de automatización de la interfaz de usuario admiten el patrón de control de [texto](uiauto-implementingtextandtextrange.md) para un control mediante la implementación de las interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) y [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Estas interfaces exponen información detallada sobre los atributos del texto del control y proporcionan capacidades de navegación sólidas.

No es necesario que un proveedor admita todos los atributos de texto si el control no tiene compatibilidad con ningún atributo determinado.

Un proveedor debe admitir los métodos [**ITextProvider:: getSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) y [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) si el control admite la selección de texto o la ubicación del cursor de texto (o símbolo de inserción) dentro del área de texto. Si el control no admite esta funcionalidad, no es necesario que admita ninguno de estos métodos. Sin embargo, el control debe exponer el tipo de selección de texto que admite implementando la propiedad [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) .

Un proveedor siempre debe admitir las constantes [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , **TextUnit \_** y **TextUnit \_**, así como cualquier otro que sea capaz de admitir.

> [!Note]  
> El proveedor puede omitir la compatibilidad con un [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) específico aplazando la siguiente unidad más grande admitida en el siguiente orden: **\_ carácter TextUnit**, **\_ formato TextUnit**, **TextUnit \_ Word**, **TextUnit \_ line**, **TextUnit \_ Paragraph**, **TextUnit \_ Page** y **TextUnit \_ Document**.

 

## <a name="client-interfaces"></a>Interfaces de cliente

Las aplicaciones cliente de automatización de la interfaz de usuario usan las interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) y [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) para tener acceso al contenido textual de un control de texto. Los clientes usan **IUIAutomationTextPattern** para seleccionar intervalos de texto denominados *intervalos de texto* y para recuperar punteros a interfaces de **IUIAutomationTextRange** para los intervalos. La interfaz **IUIAutomationTextRange** permite a los clientes manipular el intervalo de texto y recuperar información sobre el texto del intervalo, incluidos atributos como el nombre de la fuente, el color de primer plano, el estilo de subrayado, etc. Para obtener más información, vea [identificadores de atributos de texto](uiauto-textattribute-ids.md).

## <a name="performance"></a>Rendimiento

El patrón de control **Text** se basa en las llamadas entre procesos para la mayor parte de su funcionalidad, por lo que no proporciona un mecanismo de almacenamiento en caché para mejorar el rendimiento al procesar el contenido. Se puede tener acceso a otros patrones de control de la automatización de la interfaz de usuario de Microsoft mediante el método [**IUIAutomationElement:: GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) .

Una técnica para mejorar el rendimiento es asegurarse de que los clientes de automatización de la interfaz de usuario intenten recuperar bloques de texto de tamaño moderado mediante el método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) . Por ejemplo, el uso de **gettext** para recuperar caracteres individuales incurrirá en los resultados entre procesos para cada carácter, mientras que si no se especifica una longitud máxima cuando se llama a **gettext** , se producirá un acierto entre procesos, pero puede tener una latencia elevada según el tamaño del intervalo de texto.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Patrón de texto y objetos incrustados virtualizados

Siempre que sea posible, una implementación de proveedor de [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) y [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) debe admitir todo el texto de un documento, incluido cualquier texto situado fuera de la ventanilla. En el caso de texto sin pantalla o de objetos incrustados que están virtualizados, los proveedores deben admitir el [patrón de control VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Si un documento está virtualizado mientras toda la secuencia de texto sigue disponible, la propiedad [**ITextProvider::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) recuperará un intervalo de texto que incluye todo el documento. Sin embargo, al llamar al método [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) se recuperará una colección de objetos virtualizados que representan todos los objetos incrustados en el documento. Para interactuar con un objeto incrustado virtualizado, los clientes deben llamar al método [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , que hace que los elementos sean totalmente accesibles como elementos de automatización de la interfaz de usuario. Los clientes deben seguir un proceso similar para trabajar con elementos de cuadrícula en una tabla incrustada en la que una parte de la tabla está fuera de la pantalla y virtualizada.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Usar el tipo de control personalizado con el patrón de control Text

Aunque el patrón de control [Text](uiauto-implementingtextandtextrange.md) admite muchos atributos de texto y objetos incrustados, no es posible definir de antemano todos los posibles elementos de documento y tipos de presentación. En el caso de los elementos de documento que no son compatibles con los atributos existentes o los tipos de control estándar, los proveedores pueden usar las características de extensibilidad proporcionadas por el tipo de control **personalizado** de automatización de la interfaz de usuario.

En el caso de las aplicaciones y las interfaces de usuario basadas en presentaciones de páginas, el límite y la presentación de diseño de "página" también se pueden expresar como un objeto incrustado que tiene un tipo de control personalizado (es decir, `LocalizedControlType="page"` ). De este modo, el objeto incrustado puede hospedar otros elementos de página que no pueden formar parte fácilmente de la secuencia de texto del documento, como los campos de encabezado y de pie de página de cada página, como elementos secundarios del objeto incrustado de la "página". Como alternativa, cada objeto de "página" puede admitir el patrón de control de [texto](uiauto-implementingtextandtextrange.md) de forma independiente, lo que funciona bien con aplicaciones como herramientas de creación para presentaciones de presentación o entornos de publicación de escritorio basados en páginas.

## <a name="lifetime-of-a-text-range"></a>Duración de un intervalo de texto

Si es posible, un proveedor debe asegurarse de que cualquier cambio de texto, como eliminaciones, inserciones y movimientos, se refleja en el intervalo de texto asociado. Si no es posible actualizar el intervalo de texto, el proveedor debe generar un evento de [**\_ \_ TextChangedEventId de texto de UIA**](uiauto-event-ids.md) para notificar a los clientes que el intervalo de texto ya no es válido y se debe recuperar uno nuevo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Cómo la automatización de la interfaz de usuario admite objetos incrustados](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Text Services Framework (TSF)](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 