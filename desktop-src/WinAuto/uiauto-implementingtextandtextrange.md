---
title: Patrones de control Text y TextRange
description: Describe directrices y convenciones para implementar ITextProvider, ITextProvider2 e ITextRangeProvider, incluida información sobre propiedades y métodos.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Automatización de la interfaz de usuario,implementing Text control pattern
- Automatización de la interfaz de usuario, implementación del patrón de control TextRange
- Automatización de la interfaz de usuario,patrón de control Text
- Automatización de la interfaz de usuario,patrón de control TextRange
- Automatización de la interfaz de usuario,ITextProvider
- Automatización de la interfaz de usuario,ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- implementar el Automatización de la interfaz de usuario control Text
- implementación del Automatización de la interfaz de usuario de control TextRange
- Patrón de control de texto
- Patrón de control TextRange
- patrones de control,ITextProvider
- patrones de control,ITextRangeProvider
- patrones de control, implementar Automatización de la interfaz de usuario text
- patrones de control, implementar Automatización de la interfaz de usuario TextRange
- patrones de control, texto
- patrones de control,TextRange
- interfaces,ITextProvider
- interfaces,ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baf1af267e67ffe3f75a83fb970c991e9ebe5674497db2a2edad8d9cc328b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826986"
---
# <a name="text-and-textrange-control-patterns"></a>Patrones de control Text y TextRange

Describe directrices y convenciones para implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)e [**ITextRangeProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)incluida información sobre propiedades y métodos. El **patrón de** control Texto permite a las aplicaciones y los controles exponer un modelo de objetos de texto simple, lo que permite a los clientes recuperar contenido textual, atributos de texto y objetos incrustados de controles basados en texto.

Para admitir el patrón de control **Text,** los controles implementan las interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) [**e ITextProvider2.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) Los tipos de **control** que deben [](uiauto-supporteditcontroltype.md) admitir el patrón de control Texto incluyen los tipos de [control](uiauto-supportdocumentcontroltype.md) Editar y Documento, y cualquier otro tipo de control que permita al usuario escribir texto o seleccionar texto de solo lectura.

El **patrón de** control Texto se puede usar con otros patrones de control de Microsoft Automatización de la interfaz de usuario para admitir varios tipos de objetos incrustados en el texto, incluidas tablas, hipervínculos y botones de comandos.

Las [**interfaces ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) [**e ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) incluyen una serie de métodos para adquirir intervalos de texto. Un *intervalo de* texto es un objeto que representa un intervalo contiguo de texto (o varios intervalos de texto no contiguos) en un contenedor de texto. Un **método ITextProvider** adquiere un intervalo de texto que representa todo el documento, mientras que otros adquieren intervalos de texto que representan parte del documento, como el texto seleccionado, el texto visible o un objeto incrustado en el texto.

Un objeto de intervalo de texto se representa mediante el patrón de control **TextRange,** que se implementa a través de la [**interfaz ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) El patrón de control **TextRange** proporciona métodos y propiedades que se usan para exponer información sobre el texto del intervalo, mover los puntos de conexión del intervalo, seleccionar o anular la selección de texto, desplazar el intervalo a la vista, y así sucesivamente.

Para obtener más información sobre los **patrones de** control **Text y TextRange,** vea compatibilidad Automatización de la interfaz de usuario compatibilidad con contenido [textual.](uiauto-ui-automation-textpattern-overview.md)

A partir Windows 8.1 proveedores pueden implementar la [**interfaz ITextRangeProvider2.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) Esto permite invocar menús contextuales asociados a un intervalo de texto. Esto admite escenarios como la autocorrección de texto o la selección de candidatos del Editor de métodos de entrada (IME).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ITextProvider**](#required-members-for-itextprovider)
-   [Miembros necesarios para **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Admitir intervalos de texto](#supporting-text-ranges)
    -   [Manipular un intervalo de texto por unidad de texto](#manipulating-a-text-range-by-text-unit)
    -   [Selección de texto en un intervalo de texto](#selecting-text-in-a-text-range)
    -   [Adquisición de texto a partir de un intervalo de texto](#acquiring-text-from-a-text-range)
    -   [Implementación de ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilidad con el caret del sistema](#interoperability-with-the-system-caret)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Text,** tenga en cuenta las siguientes directrices y convenciones:

-   Cualquier control que permita el acceso al texto (por ejemplo, escribir texto o seleccionar texto de solo lectura) debe admitir el **patrón de** control Texto.
-   El **patrón de** control Texto se puede usar con cualquier elemento de interfaz de usuario que presente texto, incluso una etiqueta estática en un control de botón estándar. Sin embargo, no es necesario en los controles de texto estático que no se pueden seleccionar o que no tienen un punto de inserción.
-   Para asegurarse de que el texto es totalmente accesible, los controles que implementan [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) también deben admitir la [**interfaz IValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) **IValueProvider complementa** **ITextProvider proporcionando** una manera de cambiar el texto mediante programación. También ofrece una mayor compatibilidad con las aplicaciones cliente de tecnología de asistencia, incluidas las basadas en tecnologías heredadas como Microsoft Active Accessibility. Cuando se implementan ambos patrones de control, el evento **TextChanged** ([**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)) y el **evento AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) son equivalentes a la propiedad **Value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Ambos eventos deben ser compatibles.
-   El **patrón de** control Texto solo admite una secuencia de texto y una ventanilla por control. Si la aplicación ofrece varias vistas de documento en los paneles, cada vista (control) debe admitir [**ITextProvider de**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) forma independiente.
-   El [**método ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) puede devolver un único intervalo de texto que represente el texto seleccionado actualmente. Si un control admite la selección de varios intervalos de texto distintos de los siguientes, el método **GetSelection** debe devolver una matriz que contenga una interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) para cada intervalo de texto seleccionado.
-   El **patrón de** control Text representa el punto de inserción como un intervalo de texto degenerado (vacío). El [**método ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) debe devolver un intervalo de texto degenerado cuando el punto de inserción existe y no se selecciona ningún texto. Para obtener más información, vea [Interoperabilidad con el caret del sistema.](#interoperability-with-the-system-caret)
-   El [**método ITextProvider::GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) puede devolver un intervalo de texto único si un intervalo contiguo de texto está visible en la ventanilla o puede devolver una matriz de intervalos de texto no contiguos que representan varias líneas de texto parcialmente visibles.
-   El [**método ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) debe devolver un intervalo degenerado si el elemento secundario no contiene texto. Dado que un objeto incrustado puede incluir texto, es posible que el **método RangeFromChild** no siempre devuelva un intervalo de texto degenerado. Para obtener más información, [vea How Automatización de la interfaz de usuario Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).
-   El [**método ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) realiza pruebas de acceso en el área del documento mediante las coordenadas de pantalla especificadas. El intervalo de texto resultante debe ser coherente con el punto de inserción o la selección que resultaría de hacer clic en la ubicación en las coordenadas de pantalla especificadas. Por ejemplo, si una imagen reside en las coordenadas de pantalla especificadas, el intervalo de texto resultante debe ser el mismo que el intervalo de texto que el método [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) adquiriría para la imagen. De forma similar, si una aplicación cliente solicita un intervalo de texto para la ubicación en el centro del centro del sistema (el punto de inserción), el intervalo de texto resultante debe ser el mismo que el de la ubicación del elemento de inserción del sistema.
-   La [**propiedad ITextProvider::D ocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) siempre debe proporcionar un intervalo de texto que incluya todo el texto admitido por la implementación de [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) correspondiente.
-   El [**evento Text \_ \_ TextChangedEventId**](uiauto-event-ids.md) de UIA debe generarse después de que se produzca cualquier cambio de texto, incluso si el cambio no está visible en la ventanilla. Por ejemplo, el proveedor debe generar el evento incluso si el usuario pega exactamente el mismo texto sobre el texto seleccionado.
-   El [**valor de Text \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md) de UIA debe generarse siempre que cambie la selección de texto o siempre que el punto de inserción (caret) se mueva entre el texto.

Al implementar el patrón de control **TextRange,** tenga en cuenta las siguientes directrices y convenciones:

-   Todos los métodos del patrón de control **TextRange** deben realizar operaciones de texto independientemente del estado de visibilidad del texto. La visibilidad de un intervalo de texto siempre se puede determinar consultando el atributo de texto **IsHidden** ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)).
-   Si es posible, un proveedor debe asegurarse de que los cambios de texto, como eliminaciones, inserciones y movimientos, se reflejan en los objetos de intervalo de texto asociados (instancias de la interfaz [**ITextRangeProvider)**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) y generar un evento [**\_ \_ TextChangedEventId de UIA.**](uiauto-event-ids.md) Los clientes pueden usar el evento como sugerencia para confirmar los cambios editoriales realizados en el texto de un control.
-   Todos los objetos de intervalo de texto usados por los métodos [**ITextRangeProvider::Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)y [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) deben ser elementos del mismo nivel de la misma implementación del patrón de control **Text.**
-   Aunque no es necesario, el valor *pRetVal* recuperado por el método [**ITextRangeProvider::CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) puede indicar la distancia, en caracteres (carácter [**TextUnit), \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)entre los dos puntos de conexión. Sin embargo, las aplicaciones cliente no deben depender de la precisión de *pRetVal* más allá de su valor positivo o negativo.
-   Los [**métodos ITextRangeProvider::ExpandToEnclosingUnit,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)y [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) requieren una cuidadosa consideración de la unidad de texto especificada. Para obtener más información, vea Manipulating a TextRange by Text Unit.
-   Para ver los requisitos de implementación relacionados con los métodos [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)y [**RemoveFromSelection,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) vea Seleccionar texto en un intervalo de texto.
-   Los [**métodos ITextRangeProvider::FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) y [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) buscan hacia delante o hacia atrás una única cadena de texto o atributo de texto que coincida. Deben devolver **NULL si** no se encuentra ninguna coincidencia.
-   El [**método ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) debe devolver la dirección adquirida de la función [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) o [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) si el atributo asociado varía en el intervalo o si el control de texto no admite el atributo. La **especificación del patrón** de control TextRange no permite agregar nuevos identificadores de atributo de texto ni cambiar cómo se definen los atributos existentes.
-   Si es posible, el método [**ITextRangeProvider::GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) debe devolver una matriz que contenga un rectángulo delimitador para cada línea de texto totalmente o parcialmente visible en un intervalo de texto. Si esto no es posible, el proveedor puede devolver una matriz que contenga los rectángulos delimitadores de solo líneas totalmente visibles; sin embargo, esto limita la capacidad de una aplicación cliente de describir con precisión cómo se presenta el texto en la pantalla.
-   El [**método ITextRangeProvider::GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) debe devolver todos los elementos secundarios insertados en un intervalo de texto, pero no necesita devolver ningún elemento secundario de los elementos secundarios. Por ejemplo, si un intervalo de texto contiene una tabla que tiene varias celdas secundarias, el método **GetChildren** puede devolver solo el elemento table y no los elementos de celda. Por motivos de rendimiento o arquitectura, es posible que un proveedor no pueda exponer todos los objetos incrustados hospedados en un documento en el árbol de automatización. En este caso, el proveedor debe admitir al menos la enumeración de objetos secundarios mediante el método **GetChildren** y, como opción, admitir el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para la compatibilidad con la des virtualización.
-   El [**método ITextRangeProvider::GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) normalmente devuelve el proveedor de texto que proporciona el intervalo de texto. Sin embargo, si el proveedor de texto admite objetos secundarios como tablas o hipervínculos, el elemento incluido podría ser un descendiente del proveedor de texto. El elemento devuelto por **GetEnclosingElement** debe ser el elemento más cercano al intervalo de texto especificado. Por ejemplo, si el intervalo de texto está en una celda de una tabla, **GetEnclosingElement** debe devolver la celda que lo contiene en lugar del elemento table.
-   El [**método ITextRangeProvider::GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) debe devolver el texto sin formato en el intervalo. Para obtener más información, vea Adquisición de texto a partir de un intervalo de texto.
-   La [**llamada a ITextRangeProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) debe alinear el texto en la ventanilla del control de texto según lo especificado por el *parámetro alignToTop.* Aunque no hay ningún requisito en términos de alineación horizontal, el intervalo de texto debe ser visible tanto horizontal como verticalmente. Al evaluar el *parámetro alignToTop,* un proveedor debe tener en cuenta la orientación del control de texto y la dirección del flujo del texto. Por ejemplo, si *alignToTop* es **TRUE** para un control de texto orientado verticalmente que contiene texto que fluye de derecha a izquierda, el proveedor debe alinear el intervalo de texto con el lado derecho de la ventanilla.
-   Al desplazarse por un documento por [**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), si el intervalo de texto entra en una tabla incrustada, cada línea de texto de una celda debe tratarse como una línea.

## <a name="required-members-for-itextprovider"></a>Miembros necesarios para **ITextProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz ITextProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)



| Miembros requeridos                                                                                        | Tipo de miembro | Notas |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Propiedad    | Ninguno  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Propiedad    | Ninguno  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Método      | Ninguno  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Método      | Ninguno  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Método      | Ninguno  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Método      | Ninguno  |
| [**TextChangedEventId de texto UIA \_ \_**](uiauto-event-ids.md)                   | Evento       | Ninguno  |
| [**Texto de \_ \_ UIASelectionChangedEventId**](uiauto-event-ids.md) | Evento       | Ninguno  |



 

Se requieren las siguientes propiedades y métodos adicionales para implementar la [**interfaz ITextProvider2.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)



| Miembros requeridos                                                         | Tipo de miembro | Notas |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Método      | Ninguno  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Método      | Ninguno  |



 

## <a name="required-members-for-itextrangeprovider"></a>Miembros necesarios para **ITextRangeProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)



| Miembros requeridos                                                                 | Tipo de miembro | Notas |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Método      | Ninguno  |
| [**Clon**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Método      | Ninguno  |
| [**Comparar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Método      | Ninguno  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Método      | Ninguno  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Método      | Ninguno  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Método      | Ninguno  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Método      | Ninguno  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Método      | Ninguno  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Método      | Ninguno  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Método      | Ninguno  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Método      | Ninguno  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Método      | Ninguno  |
| [**Mover**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Método      | Ninguno  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Método      | Ninguno  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Método      | Ninguno  |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Método      | Ninguno  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Método      | Ninguno  |



 

Se requieren las siguientes propiedades y métodos adicionales para implementar la [**interfaz ITextRangeProvider2.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2)



| Miembros requeridos                                                      | Tipo de miembro | Notas                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Método      | Consulte la sección "Implementing ShowContextMenu" (Implementación de ShowContextMenu). |



 

El patrón de control **TextRange** no tiene eventos asociados.

## <a name="supporting-text-ranges"></a>Admitir intervalos de texto

En esta sección se describe cómo un proveedor debe implementar varios métodos de las interfaces [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) para admitir el patrón de control **TextRange.**

### <a name="manipulating-a-text-range-by-text-unit"></a>Manipular un intervalo de texto por unidad de texto

La [**interfaz ITextRangeProvider proporciona**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) varios métodos para manipular y navegar por intervalos de texto en un control basado en texto. Los métodos [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)y [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) mueven un intervalo de texto o uno de sus puntos de conexión por la unidad de texto especificada, como carácter, palabra, párrafo, y así sucesivamente. Para obtener más información, [vea Automatización de la interfaz de usuario unidades de texto](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

A pesar de su nombre, el método [**ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) no expande necesariamente un intervalo de texto. En su lugar, "normaliza" un intervalo de texto moviendo los puntos de conexión para que el intervalo abarque la unidad de texto especificada. El intervalo se expande si es menor que la unidad especificada o se acorta si es mayor que la unidad especificada. Es fundamental que el **método ExpandToEnclosingUnit** normalice siempre los intervalos de texto de forma coherente; De lo contrario, otros aspectos de la manipulación de intervalos de texto por unidad de texto serían impredecibles. En el diagrama siguiente se **muestra cómo ExpandToEnclosingUnit** normaliza un intervalo de texto moviendo los puntos de conexión del intervalo.

![diagrama que muestra las posiciones del punto de conexión del intervalo de texto antes y después de una llamada a expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Si el intervalo de texto comienza al principio de una unidad de texto y termina al principio o antes del siguiente límite de la unidad de texto, el punto de conexión final se mueve al siguiente límite de unidad de texto (vea 1 y 2 en el diagrama anterior).

Si el intervalo de texto comienza al principio de una unidad de texto y termina en el siguiente límite de unidad, o después de este, el punto de conexión final permanece o se mueve hacia atrás hasta el siguiente límite de unidad después del punto de conexión inicial (vea 3 y 4 en la ilustración anterior). Si hay más de un límite de unidad de texto entre los puntos de conexión inicial y final, el extremo final se mueve hacia atrás hasta el siguiente límite de unidad después del punto de conexión inicial, lo que da lugar a un intervalo de texto de una unidad de texto de longitud.

Si el intervalo de texto se inicia en medio de la unidad de texto, el punto de conexión inicial se mueve hacia atrás hasta el principio de la unidad de texto y el extremo final se mueve hacia delante o hacia atrás, según sea necesario, hasta el siguiente límite de unidad después del punto de conexión inicial (vea 5 a 8 en el diagrama anterior).

Cuando se llama al método [**ITextRangeProvider::Move,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) el proveedor normaliza el intervalo de texto por la unidad de texto especificada, utilizando la misma lógica de normalización que el método [**ExpandToEnclosingUnit.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) A continuación, el proveedor mueve el intervalo hacia atrás o hacia delante por el número especificado de unidades de texto. Al mover el intervalo, el proveedor debe omitir los límites de los objetos incrustados en el texto. (Sin embargo, el propio límite de unidad puede verse afectado por la existencia de un objeto incrustado). En el diagrama siguiente se muestra cómo el **método Move** mueve un intervalo de texto, unidad por unidad, entre objetos incrustados y límites de unidad de texto.

![diagrama que muestra cómo el método move mueve los puntos de conexión de intervalo entre los límites de objetos y unidades de texto](images/move.jpg)

El [**método ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) mueve uno de los puntos de conexión hacia delante o hacia atrás por la unidad de texto especificada, como se muestra en la ilustración siguiente.

![diagrama que muestra cómo moveendpointbyunit mueve el punto de conexión de un intervalo](images/moveendpointbyunit.gif)

El [**método ITextRangeProvider::MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) permite a una aplicación cliente establecer un punto de conexión de un intervalo de texto en la misma ubicación que el punto de conexión especificado de un segundo intervalo de texto.

### <a name="selecting-text-in-a-text-range"></a>Selección de texto en un intervalo de texto

La [**interfaz ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) incluye varios métodos para controlar la selección de texto en un control basado en texto.

El [**método ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) debe seleccionar el texto que corresponde a un intervalo de texto y quitar la selección anterior, si la hubiera, del control de texto. Si **se** llama a Select en un intervalo de texto degenerado, el proveedor debe mover el punto de inserción a la ubicación del intervalo de texto sin seleccionar ningún texto.

Si un control admite la selección de varios intervalos de texto no unidos, los métodos [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) y [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) agregan intervalos de texto a la colección de intervalos de texto seleccionados y los quitan de ellos. Si el control solo admite un intervalo de texto seleccionado a la vez, pero la operación de selección daría lugar a la selección de varios intervalos de texto no unidos, el proveedor debe devolver un error **E \_ INVALIDOPERATION** o extender o truncar la selección actual. La [**propiedad ITextProvider::SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) debe indicar si un control admite la selección de uno o varios intervalos de texto, o ninguno en absoluto.

Si un control basado en texto admite inserciones de texto, las llamadas a [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) o [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) en un intervalo de texto degenerado del control deben mover el punto de inserción, pero no deben seleccionar ningún texto.

### <a name="acquiring-text-from-a-text-range"></a>Adquisición de texto a partir de un intervalo de texto

El [**método ITextRangeProvider::GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) debe devolver el texto sin formato de un intervalo de texto. El texto sin formato debe incluir todos los caracteres de control encontrados en el texto de origen, como retornos de carro y la marca Unicode de izquierda a derecha (LRM). El texto sin formato no debe incluir etiquetas de marcado como HTML que puedan estar presentes en el texto de origen. Además, los códigos de escape del texto de origen deben convertirse en equivalentes de texto sin formato. Por ejemplo, " &nbsp; " se debe convertir en un carácter de espacio simple.

Si un objeto incrustado abarca un intervalo de texto, el texto sin formato debe incluir el texto interno del objeto, pero no el texto alternativo (la propiedad name del objeto incrustado) porque podría ser incoherente con el texto interno descriptivo. Para obtener más información, vea [How Automatización de la interfaz de usuario Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implementación de ShowContextMenu

[**ITextRangeProvider2::ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) siempre debe mostrar el menú contextual en el punto de conexión inicial del intervalo. Esto debería ser equivalente a lo que sucedería si el usuario presionara la tecla de menú contextual o MAYÚS + F10 con el punto de inserción al principio del intervalo.

Si mostrar el menú contextual normalmente daría lugar a que el punto de inserción se mueva a una ubicación determinada, debe hacerlo para invocar mediante programación [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) para que también Automatización de la interfaz de usuario compatibilidad.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilidad con el caret del sistema

Admitir correctamente el punto de inserción es fundamental para muchas aplicaciones cliente, incluidas las que no se basan en Automatización de la interfaz de usuario. En el **patrón de** control Texto, el punto de inserción se representa mediante un intervalo de texto degenerado (vacío) en la posición del cursor de inserción del sistema. Cuando se mueve el punto de inserción, un control debe generar el evento **TextSelectionChanged** ([**UIA \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md)). Algunas aplicaciones cliente dependen de este evento para supervisar la ubicación del punto de inserción y realizar un seguimiento de la selección de texto.

Cuando un control contiene texto seleccionado, el diseño actual del patrón de **control** Text no proporciona una manera de asociar directamente la ubicación del punto de inserción a un intervalo de texto determinado. El proveedor debe realizar un seguimiento de la selección de texto y establecer la ubicación del punto de inserción correctamente. Dado que la selección de texto se realiza normalmente moviendo el punto de inserción manteniendo presionada la tecla MAYÚS o CTRL, o ambos, un proveedor puede realizar un seguimiento de la selección de texto comprobando el estado de estas claves cada vez que cambia la selección.

Dado que el marco de accesibilidad proporciona compatibilidad integrada para el caret del sistema, pero no para un caret personalizado, los controles basados en texto deben usar el caret del sistema siempre que sea posible. Los controles que usan un elemento de inserción personalizado pueden garantizar que el elemento de inserción sea accesible mediante la creación de un caret del sistema que tenga las mismas dimensiones que el elemento de inserción personalizado y la colocación del caret del sistema en la misma ubicación de la interfaz de usuario del control que el elemento de inserción personalizado, es decir, en el punto de inserción. Como alternativa, un control que usa un caret personalizado puede implementar un proveedor de Microsoft Active Accessibility para [**OBJID \_ CARET**](object-identifiers.md) con el objeto de proporcionar información de accesibilidad directamente para el caret personalizado.

Para obtener más información sobre el caret del sistema, vea [Carets](/windows/desktop/menurc/carets).

Para comprobar si el control expone correctamente la ubicación del caret del sistema, use las herramientas [Inspeccionar](inspect-objects.md) y [Inspección](accessible-event-watcher.md) de eventos accesible.

Las coordenadas de pantalla del centro del mapa de bits del elemento de inserción del sistema siempre deben coincidir con la ubicación del punto de inserción. De este modo, un cliente puede usar las coordenadas de la pantalla de inserción en una llamada a [**ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) para recuperar un intervalo de texto que represente con precisión la ubicación del punto de inserción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tipo de control Text](uiauto-supporttextcontroltype.md)
</dt> <dt>

[TextEdit (patrón de control)](textedit-control-pattern.md)
</dt> <dt>

[Patrón de control TextChild](textchild-control-pattern.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 