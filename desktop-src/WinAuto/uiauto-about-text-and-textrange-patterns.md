---
title: Acerca de los patrones de control Text y TextRange
description: El contenido textual de un control se expone mediante el patrón de control Text, que representa el contenido de un contenedor de texto como una secuencia de texto.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Automatización de la interfaz de usuario, compatibilidad con contenido textual
- Automatización de la interfaz de usuario,text pattern overview
- Automatización de la interfaz de usuario información general sobre los controles de texto
- Automatización de la interfaz de usuario,patrón de control Text
- Automatización de la interfaz de usuario,Text Services Framework (TSF)
- Automatización de la interfaz de usuario,TSF
- Automatización de la interfaz de usuario,rendimiento
- patrones de texto, acerca de
- patrones de texto, Text Services Framework (TSF)
- controles de texto, acerca de
- contenido textual, compatibilidad con
- controles de texto, rendimiento
- Patrón de control de texto
- patrones de control, texto
- Text Services Framework (TSF)
- TSF (Text Services Framework)
- rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04112e0233db056c5ff3e81b68256229aa45f60cfdb1258e565e10aea1cd43ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052363"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Acerca de los patrones de control Text y TextRange

El contenido textual de un control se expone mediante el patrón de control [Text,](uiauto-implementingtextandtextrange.md) que representa el contenido de un contenedor de texto como una secuencia de texto. El patrón de control Text requiere la compatibilidad del patrón de control TextRange para exponer los atributos de formato y estilo. El patrón de control TextRange admite el patrón de control Text mediante la representación de intervalos de texto contiguos o múltiples e inconexos en un contenedor de texto con una colección de puntos de conexión inicial y final. El patrón de control TextRange admite funcionalidades como selección, comparación, recuperación y recorrido.

> [!Note]  
> El [patrón de](uiauto-implementingtextandtextrange.md) control Text no proporciona un medio para insertar o modificar texto. Sin embargo, dependiendo del control, esto puede realizarse mediante el patrón de control Microsoft Automatización de la interfaz de usuario [Value](uiauto-implementingvalue.md) o a través de la entrada de teclado directa. También hay un patrón [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) que admite el cambio de texto mediante programación.

 

La funcionalidad descrita en este tema es fundamental para los proveedores de tecnología de asistencia y sus usuarios finales. Las tecnologías de asistencia pueden usar Automatización de la interfaz de usuario recopilar información de formato de texto completa para el usuario y proporcionar navegación mediante programación y selección de texto por [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (carácter, palabra, línea o párrafo).

Este tema contiene las siguientes secciones:

-   [Automatización de la interfaz de usuario TextPattern y el Text Services Framework](#ui-automation-textpattern-and-the-text-services-framework)
-   [Tipos de controles](#control-types)
-   [Interfaces de proveedor](#provider-interfaces)
-   [Interfaces de cliente](#client-interfaces)
-   [Rendimiento](#performance)
-   [Patrón de texto y objetos incrustados virtualizados](#text-pattern-and-virtualized-embedded-objects)
-   [Usar el tipo de control personalizado con el patrón de control de texto](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Duración de un intervalo de texto](#lifetime-of-a-text-range)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>Automatización de la interfaz de usuario TextPattern y el Text Services Framework

Text Services Framework (TSF) es un marco de sistema sencillo y escalable que permite servicios de lenguaje natural y entrada de texto avanzada en el escritorio y en las aplicaciones. Además de proporcionar interfaces para que las aplicaciones exponan su almacén de texto, también admite metadatos para el almacén de texto.

TSF se diseñó para aplicaciones que necesitan insertar entradas en escenarios contextuales. Sin [embargo,](uiauto-implementingtextandtextrange.md) el patrón de control Texto es una solución de solo lectura que está pensada para proporcionar acceso optimizado a un almacén de texto para lectores de pantalla y dispositivos Matriz.

Las tecnologías accesibles que requieren acceso de solo lectura a un almacén de texto pueden usar el patrón de control Texto, pero necesitarán la funcionalidad de TSF para la entrada contextual.

Para obtener más información, [vea Text Services Framework](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Tipos de controles

El Automatización de la interfaz de usuario [editar](uiauto-supporteditcontroltype.md) tipo de control y [el tipo de](uiauto-supportdocumentcontroltype.md) control Documento deben admitir el patrón [de](uiauto-implementingtextandtextrange.md) control Texto. Para mejorar la accesibilidad, Microsoft recomienda que los tipos de control [Información](uiauto-supporttooltipcontroltype.md) sobre herramientas y Texto también admitan el patrón de control Texto, pero no es necesario.

## <a name="provider-interfaces"></a>Interfaces de proveedor

Automatización de la interfaz de usuario proveedores admiten el [patrón de](uiauto-implementingtextandtextrange.md) control Text para un control mediante la implementación de las interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) [**e ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) Estas interfaces exponen información detallada de atributos para el texto en el control y proporcionan funcionalidades de navegación sólidas.

Un proveedor no necesita admitir todos los atributos de texto si el control no admite ningún atributo determinado.

Un proveedor debe admitir los métodos [**ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) [**e ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) si el control admite la selección de texto o la colocación del cursor de texto (o el cursor del sistema) dentro del área de texto. Si el control no admite esta funcionalidad, no es necesario admitir ninguno de estos métodos. Sin embargo, el control debe exponer el tipo de selección de texto que admite implementando la [**propiedad ITextProvider::SupportedTextSelection.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)

Un proveedor siempre debe admitir las [**constantes TextUnit,**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) **TextUnit \_ Character** y **TextUnit \_ Document,** así como cualquier otra que sea capaz de admitir.

> [!Note]  
> El proveedor puede omitir la compatibilidad con un [**Elemento TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) específico aplazando a la siguiente unidad más grande admitida en el orden siguiente: Carácter **\_ TextUnit,** Formato **\_ TextUnit,** **TextUnit \_ Word,** **Línea TextUnit, \_** Párrafo de **\_ TextUnit,** **Página TextUnit \_** y **Documento TextUnit \_**.

 

## <a name="client-interfaces"></a>Interfaces de cliente

Automatización de la interfaz de usuario aplicaciones cliente usan las interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) para acceder al contenido textual de un control de texto. Los clientes **usan IUIAutomationTextPattern** para seleccionar intervalos de texto *denominados intervalos* de texto y para recuperar punteros a interfaces **IUIAutomationTextRange** para los intervalos. La **interfaz IUIAutomationTextRange** permite a los clientes manipular el intervalo de texto y recuperar información sobre el texto del intervalo, incluidos atributos como el nombre de fuente, el color de primer plano, el estilo de subrayado, y así sucesivamente. Para obtener más información, vea [Identificadores de atributo de texto](uiauto-textattribute-ids.md).

## <a name="performance"></a>Rendimiento

El **patrón de** control Text se basa en llamadas entre procesos para la mayor parte de su funcionalidad, por lo que no proporciona un mecanismo de almacenamiento en caché para mejorar el rendimiento al procesar el contenido. Se puede acceder a Automatización de la interfaz de usuario otros patrones de control de Microsoft mediante el [**método IUIAutomationElement::GetCachedPattern.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)

Una técnica para mejorar el rendimiento es asegurarse de que los clientes de Automatización de la interfaz de usuario intenten recuperar bloques de texto de tamaño moderado mediante el método [**IUIAutomationTextRange::GetText.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) Por ejemplo, si se usa **GetText** para recuperar caracteres únicos, se generarán aciertos entre procesos para cada carácter, mientras que si no se especifica una longitud máxima al llamar a **GetText,** se incurrirá en un acierto entre procesos, pero puede tener una latencia alta en función del tamaño del intervalo de texto.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Patrón de texto y objetos incrustados virtualizados

Siempre que sea posible, una implementación de proveedor de [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) debe admitir todo el texto de un documento, incluido cualquier texto fuera de la ventanilla. En el caso del texto fuera de la pantalla o los objetos incrustados que están virtualizados, los proveedores deben admitir el patrón de [control VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Si un documento se virtualiza mientras la secuencia de texto completa sigue estando disponible, la propiedad [**ITextProvider::D ocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) recuperará un intervalo de texto que incluya todo el documento. Sin embargo, al llamar [**al método ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) se recuperará una colección de objetos virtualizados que representan todos los objetos incrustados en el documento. Para interactuar con un objeto incrustado virtualizado, los clientes deben llamar al método [**IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) lo que hace que los elementos sea totalmente accesibles Automatización de la interfaz de usuario elementos. Los clientes deben seguir un proceso similar para trabajar con elementos de cuadrícula en una tabla insertada en la que una parte de la tabla está fuera de la pantalla y virtualizada.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Usar el tipo de control personalizado con el patrón de control de texto

Aunque el [patrón de](uiauto-implementingtextandtextrange.md) control Texto admite muchos atributos de texto y objetos incrustados, no es posible definir de antemano todos los elementos de documento y tipos de presentación posibles. Para los elementos de documento que no son compatibles con los atributos existentes o los tipos de control estándar, los proveedores pueden usar las características de extensibilidad proporcionadas por el Automatización de la interfaz de usuario **de** control Personalizado.

En el caso de las aplicaciones y las interfaces de usuario que se basan en presentaciones de página, el límite y la presentación de diseño de "página" también se pueden expresar como un objeto incrustado que tiene un tipo de control personalizado (es decir, `LocalizedControlType="page"` ). De este modo, el objeto incrustado puede hospedar otros elementos de página que no pueden formar parte fácilmente de la secuencia de texto del documento, como los campos de encabezado y pie de página de cada página, como elementos secundarios del objeto incrustado "página". Como alternativa, cada objeto de "página" puede admitir el patrón de [control](uiauto-implementingtextandtextrange.md) Texto de forma independiente, lo que funciona bien para aplicaciones como herramientas de creación para presentaciones de diapositivas o entornos de publicación de escritorio basados en páginas.

## <a name="lifetime-of-a-text-range"></a>Duración de un intervalo de texto

Si es posible, un proveedor debe asegurarse de que los cambios de texto, como eliminaciones, inserciones y movimientos, se reflejen en el intervalo de texto asociado. Si no es posible actualizar el intervalo de texto, el proveedor debe generar un evento [**\_ \_ TextChangedEventId**](uiauto-event-ids.md) de UIA para notificar a los clientes que el intervalo de texto ya no es válido y que se debe recuperar uno nuevo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Compatibilidad Automatización de la interfaz de usuario objetos incrustados](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Text Services Framework (TSF)](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 