---
title: Patrones de control Text y TextRange
description: Describe las directrices y convenciones para implementar ITextProvider, ITextProvider2 y ITextRangeProvider, incluida información sobre propiedades y métodos.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Text
- Automatización de la interfaz de usuario, implementar el patrón de control TextRange
- Automatización de la interfaz de usuario, patrón de control Text
- Automatización de la interfaz de usuario, patrón de control TextRange
- Automatización de la interfaz de usuario, ITextProvider
- Automatización de la interfaz de usuario, ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- implementar el patrón de control Text de UI Automation
- implementar el patrón de control TextRange de automatización de la interfaz de usuario
- Text (patrón de control)
- TextRange (patrón de control)
- patrones de control, ITextProvider
- patrones de control, ITextRangeProvider
- patrones de control, implementar texto de automatización de la interfaz de usuario
- patrones de control, implementar la automatización de la interfaz de usuario
- patrones de control, texto
- patrones de control, TextRange
- interfaces, ITextProvider
- interfaces, ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53429dc8ec137a83b6a40db377b5c84aeb36120
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555463"
---
# <a name="text-and-textrange-control-patterns"></a>Patrones de control Text y TextRange

Describe las directrices y convenciones para implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)y [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), incluida información sobre propiedades y métodos. El patrón de control **Text** permite a las aplicaciones y los controles exponer un modelo de objetos de texto simple, lo que permite a los clientes recuperar contenido textual, atributos de texto y objetos incrustados de controles basados en texto.

Para admitir el patrón de control **Text** , los controles implementan las interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) y [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) . Los tipos de control que deben admitir el patrón de control **Text** incluyen los tipos de control de [edición](uiauto-supporteditcontroltype.md) y de [documento](uiauto-supportdocumentcontroltype.md) , así como cualquier otro tipo de control que permita al usuario escribir texto o seleccionar texto de solo lectura.

El patrón de control **Text** se puede usar con otros patrones de control de automatización de la interfaz de usuario de Microsoft para admitir varios tipos de objetos incrustados en el texto, como tablas, hipervínculos y botones de comando.

Las interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) y [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) incluyen una serie de métodos para la adquisición de intervalos de texto. Un *intervalo de texto* es un objeto que representa un intervalo contiguo de texto, o varios intervalos separados de texto, en un contenedor de texto. Un método **ITextProvider** adquiere un intervalo de texto que representa todo el documento, mientras que otros usuarios adquieren intervalos de texto que representan parte del documento, como el texto seleccionado, el texto visible o un objeto incrustado en el texto.

Un objeto de intervalo de texto se representa mediante el patrón de control **TextRange** , que se implementa a través de la interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . El patrón de control **TextRange** proporciona métodos y propiedades que se usan para exponer información sobre el texto del intervalo, para desplazar los extremos del intervalo, seleccionar o anular la selección de texto, desplazar el rango a la vista, etc.

Para obtener más información sobre los patrones de control **Text** y **TextRange** , vea [compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md).

A partir de Windows 8.1 los proveedores pueden implementar la interfaz [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) . Esto permite invocar menús contextuales que están asociados a un intervalo de texto. Esto es compatible con escenarios como la corrección de texto o la selección candidata del editor de métodos de entrada (IME).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **ITextProvider**](#required-members-for-itextprovider)
-   [Miembros requeridos para **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Intervalos de texto compatibles](#supporting-text-ranges)
    -   [Manipular un intervalo de texto por unidad de texto](#manipulating-a-text-range-by-text-unit)
    -   [Seleccionar texto en un intervalo de texto](#selecting-text-in-a-text-range)
    -   [Adquirir texto de un intervalo de texto](#acquiring-text-from-a-text-range)
    -   [Implementación de ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilidad con el símbolo de intercalación del sistema](#interoperability-with-the-system-caret)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Text** , tenga en cuenta las siguientes directrices y convenciones:

-   Cualquier control que permita el acceso a texto (por ejemplo, al escribir texto o seleccionar texto de solo lectura) debe admitir el patrón de control **Text** .
-   El patrón de control **Text** se puede usar con cualquier elemento de la interfaz de usuario que presente texto, incluso una etiqueta estática en un control de botón estándar. Sin embargo, no es necesario en los controles de texto estático que no se pueden seleccionar o no tienen un punto de inserción.
-   Para asegurarse de que el texto es totalmente accesible, los controles que implementan [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) también deben admitir la interfaz [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) . **IValueProvider** complementa **ITextProvider** proporcionando una manera programática de cambiar el texto. También ofrece mayor compatibilidad con las aplicaciones cliente de tecnología de asistencia, incluidas las basadas en tecnologías heredadas como Microsoft Active Accessibility. Cuando se implementan ambos patrones de control, el evento **TextChanged** ([**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)) y el evento **AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) son equivalentes a la propiedad **Value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Ambos eventos deben ser compatibles.
-   El patrón de control **Text** solo admite un flujo de texto y una ventanilla por control. Si la aplicación ofrece varias vistas de documento en paneles, cada vista (control) debe admitir [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) de forma independiente.
-   El método [**ITextProvider:: getSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) puede devolver un solo intervalo de texto que representa el texto seleccionado actualmente. Si un control admite la selección de varios intervalos de texto no contiguos, el método **getSelection** debe devolver una matriz que contenga una interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) para cada intervalo de texto seleccionado.
-   El patrón de control **Text** representa el punto de inserción como un intervalo de texto degenerado (vacío). El método [**ITextProvider:: getSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) debe devolver un intervalo de texto degenerado cuando el punto de inserción existe y no se ha seleccionado ningún texto. Para obtener más información, consulte [interoperabilidad con el símbolo de intercalación del sistema](#interoperability-with-the-system-caret).
-   El método [**ITextProvider:: GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) puede devolver un solo intervalo de texto si hay un intervalo de texto contiguo visible en la ventanilla, o puede devolver una matriz de intervalos de texto separados que representan varias líneas de texto visibles parcialmente.
-   El método [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) debe devolver un intervalo degenerado si el elemento secundario no contiene texto. Dado que un objeto incrustado puede incluir texto, el método **RangeFromChild** no siempre devuelve un intervalo de texto degenerado. Para obtener más información, vea [cómo la automatización de la interfaz de usuario expone objetos incrustados](uiauto-textpattern-and-embedded-objects-overview.md).
-   El método [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) realiza la prueba de posicionamiento en el área de documento usando las coordenadas de pantalla especificadas. El intervalo de texto resultante debe ser coherente con el punto de inserción o la selección que resultaría de hacer clic en la ubicación en las coordenadas de pantalla especificadas. Por ejemplo, si una imagen se encuentra en las coordenadas de pantalla especificadas, el intervalo de texto resultante debe ser el mismo que el intervalo de texto que el método [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) adquiriría para la imagen. Del mismo modo, si una aplicación cliente solicita un intervalo de texto para la ubicación en el centro del símbolo de intercalación del sistema (punto de inserción), el intervalo de texto resultante debe ser el mismo que el de la ubicación del símbolo de intercalación del sistema.
-   La propiedad [**ITextProvider::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) siempre debe proporcionar un intervalo de texto que incluya todo el texto admitido por la implementación [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) correspondiente.
-   El [**evento \_ \_ TextChangedEventId de texto de UIA**](uiauto-event-ids.md) debe generarse después de que se produzca cualquier cambio de texto, aunque el cambio no esté visible en la ventanilla. Por ejemplo, el proveedor debe generar el evento incluso si el usuario pega exactamente el mismo texto sobre el texto seleccionado.
-   El [**\_ \_ TextSelectionChangedEventId de texto de UIA**](uiauto-event-ids.md) debe generarse cada vez que cambie la selección de texto, o cada vez que el punto de inserción (símbolo de intercalación) se mueva entre el texto.

Al implementar el patrón de control **TextRange** , tenga en cuenta las siguientes directrices y convenciones:

-   Todos los métodos del patrón de control **TextRange** deben realizar operaciones de texto independientemente del estado de visibilidad del texto. La visibilidad de un intervalo de texto siempre se puede determinar consultando el atributo de texto **IsHidden** ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)).
-   Si es posible, un proveedor debe asegurarse de que cualquier cambio de texto, como eliminaciones, inserciones y movimientos, se refleja en los objetos de intervalo de texto asociados (instancias de la interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ) y genera un evento de [**\_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) . Los clientes pueden usar el evento como una sugerencia para confirmar los cambios editoriales realizados en el texto de un control.
-   Todos los objetos de intervalo de texto utilizados por los métodos [**ITextRangeProvider:: Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)y [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) deben ser del mismo nivel que la implementación del patrón de control **Text** .
-   Aunque no es necesario, el valor *pRetVal* recuperado por el método [**ITextRangeProvider:: CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) puede indicar la distancia, en caracteres ([**\_ carácter TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)), entre los dos extremos. Sin embargo, las aplicaciones cliente no deben depender de la precisión de *pRetVal* más allá de su valor positivo o negativo.
-   Los métodos [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit), [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)y [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) requieren una consideración cuidadosa de la unidad de texto especificada. Para obtener más información, vea manipular un TextRange por unidad de texto.
-   Para conocer los requisitos de implementación relacionados con los métodos [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)y [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) , consulte Seleccionar texto en un intervalo de texto.
-   Los métodos [**ITextRangeProvider:: FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) y [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) buscan hacia delante o hacia atrás para una sola cadena de texto o atributo de texto coincidente. Deben devolver **null** si no se encuentra ninguna coincidencia.
-   El método [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) debe devolver la dirección adquirida a partir de la función [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) o [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) si el atributo asociado varía en el intervalo o si el control de texto no admite el atributo. La especificación del patrón de control **TextRange** no permite agregar nuevos identificadores de atributo de texto ni cambiar la definición de los atributos existentes.
-   Si es posible, el método [**ITextRangeProvider:: GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) debe devolver una matriz que contenga un rectángulo delimitador para cada línea de texto total o parcialmente visible en un intervalo de texto. Si esto no es posible, el proveedor puede devolver una matriz que contenga los rectángulos delimitadores de solo líneas totalmente visibles; sin embargo, esto limita la capacidad de una aplicación cliente para describir con precisión el modo en que se presenta el texto en la pantalla.
-   El método [**ITextRangeProvider:: GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) debe devolver todos los elementos secundarios incrustados en un intervalo de texto, pero no es necesario devolver ningún elemento secundario de los elementos secundarios. Por ejemplo, si un intervalo de texto contiene una tabla que tiene un número de celdas secundarias, el método **GetChildren** solo puede devolver el elemento TABLE y no los elementos Cell. Por motivos de rendimiento o arquitectura, es posible que un proveedor no pueda exponer todos los objetos incrustados que se hospedan en un documento en el árbol de automatización. En este caso, el proveedor debe admitir al menos la enumeración de los objetos secundarios a través del método **GetChildren** y, como opción, admite el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para la compatibilidad con la desvirtualización.
-   El método [**ITextRangeProvider:: GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) devuelve normalmente el proveedor de texto que proporciona el intervalo de texto. Sin embargo, si el proveedor de texto admite objetos secundarios como tablas o hipervínculos, el elemento envolvente podría ser un descendiente del proveedor de texto. El elemento devuelto por **GetEnclosingElement** debe ser el elemento más cercano al intervalo de texto especificado. Por ejemplo, si el intervalo de texto está en una celda de una tabla, **GetEnclosingElement** debe devolver la celda que lo contiene en lugar del elemento TABLE.
-   El método [**ITextRangeProvider:: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) debe devolver el texto sin formato del intervalo. Para obtener más información, vea adquirir texto de un intervalo de texto.
-   La llamada a [**ITextRangeProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) debe alinear el texto en la ventanilla del control de texto tal y como se especifica en el parámetro *alignToTop* . Aunque no hay ningún requisito en cuanto a la alineación horizontal, el intervalo de texto debe estar visible tanto horizontal como verticalmente. Al evaluar el parámetro *alignToTop* , un proveedor debe tener en cuenta la orientación del control de texto y la dirección de flujo del texto. Por ejemplo, si *alignToTop* es **true** para un control de texto orientado verticalmente que contiene texto que fluye de derecha a izquierda, el proveedor debe alinear el intervalo de texto con el lado derecho de la ventanilla.
-   Al desplazarse por un documento por la [**\_ línea TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), si el intervalo de texto entra en una tabla incrustada, cada línea de texto de una celda se debe tratar como una línea.

## <a name="required-members-for-itextprovider"></a>Miembros requeridos para **ITextProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) .



| Miembros requeridos                                                                                        | Tipo de miembro | Notas |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Propiedad    | None  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Propiedad    | None  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Método      | None  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Método      | None  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Método      | None  |
| [**Tal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Método      | None  |
| [**\_TextChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                   | Evento       | None  |
| [**\_TextSelectionChangedEventId de texto de UIA \_**](uiauto-event-ids.md) | Evento       | None  |



 

Se requieren las siguientes propiedades y métodos adicionales para implementar la interfaz [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) .



| Miembros requeridos                                                         | Tipo de miembro | Notas |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Método      | None  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Método      | None  |



 

## <a name="required-members-for-itextrangeprovider"></a>Miembros requeridos para **ITextRangeProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) .



| Miembros requeridos                                                                 | Tipo de miembro | Notas |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Método      | None  |
| [**Clonar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Método      | None  |
| [**Comparar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Método      | None  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Método      | None  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Método      | None  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Método      | None  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Método      | None  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Método      | None  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Método      | None  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Método      | None  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Método      | None  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Método      | None  |
| [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Método      | None  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Método      | None  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Método      | None  |
| [**Seleccionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Método      | None  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Método      | None  |



 

Se requieren las siguientes propiedades y métodos adicionales para implementar la interfaz [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) .



| Miembros requeridos                                                      | Tipo de miembro | Notas                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Método      | Vea la sección "implementación de ShowContextMenu". |



 

El patrón de control **TextRange** no tiene eventos asociados.

## <a name="supporting-text-ranges"></a>Intervalos de texto compatibles

En esta sección se describe cómo un proveedor debe implementar varios métodos de las interfaces [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) y [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) para admitir el patrón de control **TextRange** .

### <a name="manipulating-a-text-range-by-text-unit"></a>Manipular un intervalo de texto por unidad de texto

La interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) proporciona varios métodos para manipular y navegar por los intervalos de texto en un control basado en texto. Los métodos [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)y [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) mueven un intervalo de texto o uno de sus extremos por la unidad de texto especificada, como carácter, palabra, párrafo, etc. Para obtener más información, consulte [UI Automation Text Units](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

A pesar de su nombre, el método [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) no expande necesariamente un intervalo de texto. En su lugar, "normaliza" un intervalo de texto moviendo los puntos de conexión para que el intervalo abarque la unidad de texto especificada. El intervalo se expande si es menor que la unidad especificada o se acorta si es mayor que la unidad especificada. Es fundamental que el método **ExpandToEnclosingUnit** siempre normalice los intervalos de texto de una manera coherente. de lo contrario, otros aspectos de la manipulación del intervalo de texto por unidad de texto serían imprevisibles. En el diagrama siguiente se muestra cómo **ExpandToEnclosingUnit** normaliza un intervalo de texto moviendo los extremos del intervalo.

![diagrama que muestra las posiciones de punto de conexión del intervalo de texto antes y después de una llamada a expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Si el intervalo de texto comienza al principio de una unidad de texto y termina al principio del límite de unidad de texto siguiente, o antes, el extremo final se mueve al siguiente límite de unidad de texto (vea 1 y 2 en el diagrama anterior).

Si el intervalo de texto comienza al principio de una unidad de texto y termina en el siguiente límite de unidad, o después, el extremo final permanece o se mueve hacia atrás hasta el siguiente límite de unidad después del punto de conexión de inicio (vea 3 y 4 en la ilustración anterior). Si hay más de un límite de unidad de texto entre los puntos de conexión inicial y final, el extremo final se desplaza hacia atrás hasta el siguiente límite de unidad después del punto de conexión de inicio, lo que da lugar a un intervalo de texto que es una unidad de texto de longitud.

Si el intervalo de texto se inicia en medio de la unidad de texto, el punto de conexión inicial se desplaza hacia atrás hasta el principio de la unidad de texto y el extremo final se mueve hacia delante o hacia atrás, según sea necesario, al siguiente límite de unidad después del punto de conexión de inicio (vea 5 a 8 en el diagrama anterior).

Cuando se llama al método [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) , el proveedor normaliza el intervalo de texto por la unidad de texto especificada, usando la misma lógica de normalización que el método [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) . A continuación, el proveedor mueve el intervalo hacia atrás o hacia delante el número especificado de unidades de texto. Al mover el intervalo, el proveedor debe omitir los límites de cualquier objeto incrustado en el texto. (Sin embargo, el propio límite de unidad puede verse afectado por la existencia de un objeto incrustado). En el diagrama siguiente se muestra cómo el método **Move** mueve un intervalo de texto, unidad por unidad, entre los objetos incrustados y los límites de la unidad de texto.

![diagrama que muestra cómo el método move mueve los extremos de intervalo entre los límites de unidad de texto y objeto](images/move.jpg)

El método [**ITextRangeProvider:: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) mueve uno de los extremos hacia delante o hacia atrás por la unidad de texto especificada, como se muestra en la ilustración siguiente.

![diagrama que muestra cómo moveendpointbyunit mueve el punto de conexión de un intervalo](images/moveendpointbyunit.gif)

El método [**ITextRangeProvider:: MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) permite a una aplicación cliente establecer un punto de conexión de un intervalo de texto en la misma ubicación que el punto de conexión especificado de un segundo intervalo de texto.

### <a name="selecting-text-in-a-text-range"></a>Seleccionar texto en un intervalo de texto

La interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) incluye varios métodos para controlar la selección de texto en un control basado en texto.

El método [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) debe seleccionar el texto que corresponde a un intervalo de texto y quitar la selección anterior, si existe, del control de texto. Si se llama a **Select** en un intervalo de texto degenerado, el proveedor debe trasladar el punto de inserción a la ubicación del intervalo de texto sin seleccionar ningún texto.

Si un control admite la selección de varios intervalos separados de texto, los métodos [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) y [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) agregan intervalos de texto a y los quita de la colección de intervalos de texto seleccionados. Si el control solo admite un intervalo de texto seleccionado cada vez, pero la operación de selección daría lugar a la selección de varios intervalos de texto disjuntos, el proveedor debe devolver un error **E \_ INVALIDOPERATION** , o bien debe extender o truncar la selección actual. La propiedad [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) debe indicar si un control admite la selección de uno o varios intervalos de texto o ninguno.

Si un control basado en texto admite inserciones de texto, al llamar a [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) o [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) en un intervalo de texto degenerado en el control, se debe desplace el punto de inserción pero no se debe seleccionar ningún texto.

### <a name="acquiring-text-from-a-text-range"></a>Adquirir texto de un intervalo de texto

El método [**ITextRangeProvider:: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) debe devolver el texto sin formato de un intervalo de texto. El texto sin formato debe incluir todos los caracteres de control que se encuentran en el texto de origen, como retornos de carro y la marca de izquierda a derecha (LRM) de Unicode. El texto sin formato no debe incluir etiquetas de marcado, como HTML, que puedan estar presentes en el texto de origen. Además, los códigos de escape del texto de origen deben convertirse en los equivalentes de texto sin formato. Por ejemplo, " &nbsp; " se debe convertir en un carácter de espacio simple.

Si un objeto incrustado abarca un intervalo de texto, el texto sin formato debe incluir el texto interno del objeto, pero no el texto alternativo (la propiedad nombre del objeto incrustado) porque podría no ser coherente con el texto interno descriptivo. Para obtener más información, vea [cómo la automatización de la interfaz de usuario expone objetos incrustados](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implementación de ShowContextMenu

[**ITextRangeProvider2:: ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) siempre debe mostrar el menú contextual en el extremo inicial del intervalo. Debe ser equivalente a lo que sucedería si el usuario presionara la tecla del menú contextual o Mayús + F10 con el punto de inserción al principio del intervalo.

Si se muestra el menú contextual, por lo general, el punto de inserción se traslada a una ubicación determinada y, a continuación, debería hacerlo para invocar mediante programación [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) para la compatibilidad con la automatización de la interfaz de usuario.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilidad con el símbolo de intercalación del sistema

La compatibilidad correcta con el punto de inserción es fundamental para muchas aplicaciones cliente, incluidas las que no se basan en la automatización de la interfaz de usuario. En el patrón de control **Text** , el punto de inserción se representa mediante un intervalo de texto degenerado (vacío) en la posición del símbolo de intercalación del sistema. Cuando se mueve el punto de inserción, un control debe generar el evento **TextSelectionChanged** ([**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)). Algunas aplicaciones cliente dependen de este evento para supervisar la ubicación del punto de inserción y para realizar un seguimiento de la selección de texto.

Cuando un control contiene texto seleccionado, el diseño actual del patrón de control **Text** no proporciona una manera de asociar directamente la ubicación del punto de inserción con un intervalo de texto determinado. El proveedor debe realizar un seguimiento de la selección de texto y establecer la ubicación del punto de inserción de forma adecuada. Dado que la selección de texto se realiza normalmente moviendo el punto de inserción mientras mantiene presionada la tecla Mayús o CTRL, o ambos, un proveedor puede realizar el seguimiento de la selección de texto comprobando el estado de estas claves cada vez que cambie la selección.

Dado que el marco de accesibilidad proporciona compatibilidad integrada para el símbolo de intercalación del sistema, pero no para un símbolo de intercalación personalizado, los controles basados en texto deben usar el símbolo de intercalación del sistema siempre que sea posible. Los controles que usan un símbolo de intercalación personalizado pueden asegurarse de que se puede obtener acceso al símbolo de intercalación creando un símbolo de intercalación del sistema que tenga las mismas dimensiones que el símbolo de intercalación personalizado y colocando el símbolo de intercalación del sistema en la misma ubicación en la interfaz de usuario del control que el símbolo de intercalación personalizado Como alternativa, un control que usa un símbolo de intercalación personalizado puede implementar un proveedor de Active Accessibility de Microsoft para el [**\_ símbolo de intercalación de OBJID**](object-identifiers.md) para proporcionar información de accesibilidad directamente para el símbolo de intercalación personalizado.

Para obtener más información sobre el símbolo de intercalación del sistema, consulte [Cares](/windows/desktop/menurc/carets).

Para probar si el control expone correctamente la ubicación del símbolo de intercalación del sistema, utilice las herramientas [inspeccionar](inspect-objects.md) y [monitor de eventos accesibles](accessible-event-watcher.md) .

Las coordenadas de pantalla del centro del mapa de bits del símbolo de intercalación del sistema siempre deben coincidir con la ubicación del punto de inserción. De este modo, un cliente puede usar las coordenadas de la pantalla del símbolo de intercalación en una llamada a [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) para recuperar un intervalo de texto que represente con precisión la ubicación del punto de inserción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Text (tipo de control)](uiauto-supporttextcontroltype.md)
</dt> <dt>

[Patrón de control TextEdit](textedit-control-pattern.md)
</dt> <dt>

[Patrón de control TextChild](textchild-control-pattern.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 