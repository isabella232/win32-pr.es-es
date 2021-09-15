---
title: Patrón de control Annotation
description: Describe directrices y convenciones para implementar IAnnotationProvider, incluida información sobre propiedades y métodos. El patrón de control Annotation se usa para exponer las propiedades de una anotación en un documento.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control de anotación
- Automatización de la interfaz de usuario,patrón de control de anotación
- Automatización de la interfaz de usuario,IAnnotationProvider
- IAnnotationProvider
- implementación de un Automatización de la interfaz de usuario de control de anotación
- patrón de control de anotación
- patrones de control,IAnnotationProvider
- patrones de control, implementar Automatización de la interfaz de usuario anotación
- patrones de control, anotación
- interfaces,IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a0441816e548faaa9076b3a9717c0aa76f08a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567253"
---
# <a name="annotation-control-pattern"></a>Patrón de control Annotation

Describe directrices y convenciones para implementar [**IAnnotationProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)incluida información sobre propiedades y métodos. El **patrón de** control Annotation se usa para exponer las propiedades de una anotación en un documento.

Un ejemplo es un globo de comentarios que está en el margen de un documento y está conectado a algún texto del documento o a una celda de hoja de cálculo.

En la ilustración siguiente se muestra un ejemplo de una anotación. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

![captura de pantalla que muestra un comentario en un documento](images/annotation.png)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IAnnotationProvider**](#required-members-for-iannotationprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Annotation,** tenga en cuenta las siguientes directrices y convenciones:

-   Hay muchos tipos diferentes de anotaciones. El archivo de encabezado UIAutomationClient.h define un conjunto de valores constantes con nombre que identifican los tipos de anotaciones que admite Microsoft Automatización de la interfaz de usuario. Para obtener más información, vea [**Annotation Type Identifiers**](uiauto-annotation-type-identifiers.md).
-   Si usa [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md), debe implementar la propiedad [**IAnnotationProvider::AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) para permitir que los clientes detecten el nombre del tipo de anotación. No es necesario implementar **AnnotationTypeName** para un tipo de anotación estándar porque Automatización de la interfaz de usuario proporciona un nombre predeterminado, pero puede implementarlo si necesita invalidar el nombre predeterminado.
-   La [**propiedad IAnnotationProvider::Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) es opcional.
-   La [**propiedad IAnnotationProvider::D ateTime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) es opcional.
-   La [**propiedad IAnnotationProvider::Target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) es necesaria porque vincula una anotación a un elemento de la interfaz de usuario, lo que permite a un cliente navegar desde la anotación hasta el elemento de interfaz de usuario al que hace referencia la anotación.
-   Dado que las anotaciones pueden tomar muchas formas diferentes, la [**interfaz IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) no define una propiedad para almacenar el valor o el texto de una anotación. Una anotación simple debe exponer la interfaz [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) y la propiedad [**IValueProvider::Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) debe devolver un valor de solo lectura que especifique el texto de la anotación. Una anotación más enriquección debe exponer [**la interfaz ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) para proporcionar texto más enriquecido a los clientes.
-   La navegación desde un elemento de la interfaz de usuario a una anotación en el elemento depende del tipo de elemento anotado, como se indica a continuación:
    -   Para las celdas de hoja de cálculo, implemente el método [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) para hacer referencia a la anotación.
    -   Para el contenido textual, implemente el atributo de texto [**AnnotationObjects**](uiauto-textattribute-ids.md) en la [**interfaz ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) para hacer referencia a la anotación.
-   Algunos tipos de anotaciones no requieren una implementación completa de la [**interfaz IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Por ejemplo, un indicador de error ortográfico simple podría representarse haciendo que la interfaz [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) devuelva un atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) [**de AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)y un valor NULL para el atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
-   Puede ser útil implementar la interfaz [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) en un elemento de interfaz de usuario que no está visible. Por ejemplo, podría crear un elemento Automatización de la interfaz de usuario no visible que implemente **IAnnotationProvider** para proporcionar información extendida sobre un error de gramática.
-   Las anotaciones de un control basado en texto pueden ser complejas si el control contiene comentarios superpuestos. Use las siguientes directrices para controlar anotaciones complejas:
    -   Un intervalo de texto sin anotaciones debe devolver una matriz vacía para el atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) y una matriz vacía para el atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Un intervalo de texto con una anotación debe devolver una matriz de un valor entero para el atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) y una matriz de una interfaz [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para el atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Un intervalo de texto con varias anotaciones debe devolver una matriz de varios valores enteros para el atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) y una matriz de un número correspondiente de interfaces [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para el atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Un intervalo de texto con anotaciones variables, como un intervalo con texto anotado y no anotado, debe devolver la propiedad [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) para [**AnnotationTypes**](uiauto-textattribute-ids.md) y [**AnnotationObjects**](uiauto-textattribute-ids.md). Un cliente que recibe esta respuesta puede subdividir el intervalo de texto para encontrar dónde comienzan y terminan las anotaciones.

## <a name="required-members-for-iannotationprovider"></a>Miembros necesarios para **IAnnotationProvider**

Las siguientes propiedades son necesarias para implementar la [**interfaz IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)



| Miembros requeridos                                                                | Tipo de miembro | Notas |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Propiedad    | Ninguno. |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Propiedad    | Ninguno. |
| [**Autor**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Propiedad    | Ninguno. |
| [**Datetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Propiedad    | Ninguno. |
| [**Destino**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Propiedad    | Ninguno. |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 