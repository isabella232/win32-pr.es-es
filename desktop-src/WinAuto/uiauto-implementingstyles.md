---
title: Patrón de control Estilos
description: Describe directrices y convenciones para implementar IStylesProvider, incluida información sobre propiedades y métodos. El patrón de control Estilos se usa para describir un elemento de interfaz de usuario que tiene un estilo, un color de relleno, un patrón de relleno o una forma específicos.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Estilos
- Automatización de la interfaz de usuario,Patrón de control Estilos
- Automatización de la interfaz de usuario,IStylesProvider
- IStylesProvider
- implementar el patrón de control Automatización de la interfaz de usuario estilos de usuario
- Patrón de control Estilos
- patrones de control,IStylesProvider
- patrones de control, implementar Automatización de la interfaz de usuario estilos
- patrones de control, estilos
- interfaces,IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e52a6829e592cc659d5ce47b51a09b6d8910d4bd2c41a1e03c9b661d027fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324093"
---
# <a name="styles-control-pattern"></a>Patrón de control Estilos

Describe directrices y convenciones para implementar [**IStylesProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider)incluida información sobre propiedades y métodos. El **patrón de** control Estilos se usa para describir un elemento de interfaz de usuario que tiene un estilo, un color de relleno, un patrón de relleno o una forma específicos.

El **patrón de** control Estilos es especialmente útil para describir elementos de un documento, que con frecuencia tienen estos estilos. Los estilos suelen llevar información útil para los clientes con discapacidades. Por ejemplo, un estilo puede describir una cadena determinada como el título de un documento o un determinado objeto de diagrama de flujo como un rombo o un círculo. Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IStylesProvider**](#required-members-for-istylesprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Estilos,** tenga en cuenta las siguientes directrices y convenciones:

-   El archivo de encabezado UIAutomationClient.h define un conjunto de valores constantes con nombre que se usan para identificar varios estilos comunes. Para obtener más información, vea [**Identificadores de estilo**](uiauto-style-identifiers.md).
-   Si usa [**StyleId \_ personalizado,**](uiauto-style-identifiers.md)debe implementar la propiedad [**IStylesProvider::StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que los clientes detecten el nombre del estilo. No es necesario implementar la propiedad **StyleName** para un estilo estándar porque Microsoft Automatización de la interfaz de usuario proporciona un nombre predeterminado, pero puede implementarlo si necesita invalidar el nombre predeterminado.
-   Las demás propiedades del patrón **Styles son** opcionales; el proveedor puede devolver [**UIA \_ E \_ NOTSUPPORTED para**](uiauto-error-codes.md) una propiedad que no se admite.
-   Los estilos de un intervalo de texto se pueden representar mediante los siguientes atributos de texto:
    -   Al responder a una solicitud para el atributo de texto [**StyleId,**](uiauto-textattribute-ids.md) el intervalo de texto debe devolver uno de los identificadores de estilo descritos en [**Identificadores de estilo**](uiauto-style-identifiers.md).
    -   Si [**se usa StyleId \_ Custom,**](uiauto-style-identifiers.md) el intervalo de texto debe devolver un valor de cadena para el atributo de texto [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir a los clientes detectar el nombre de estilo.
    -   Un intervalo de texto con varios estilos, como el encabezado y el texto normal, debe devolver la propiedad Automatización de la interfaz de usuario [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) especial para las propiedades [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) y [**StyleName.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) Un cliente que recibe esta respuesta puede subdividir el intervalo de texto para encontrar dónde comienzan y terminan los estilos.
-   Las aplicaciones pueden usar una amplia variedad de estilos para describir objetos, Automatización de la interfaz de usuario solo representa los más comunes. Para representar atributos de estilo adicionales, como el color del borde, un proveedor puede devolver una lista de atributos adicionales en la [**propiedad ExtendedProperties.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) Básicamente se trata de un bolsa de propiedades con un conjunto de propiedades extendidas, como "BorderColor=0xFF0000; BorderStyle=dotted". Los valores de las propiedades extendidas pueden ser específicos de la aplicación.

## <a name="required-members-for-istylesprovider"></a>Miembros necesarios para **IStylesProvider**

Las siguientes propiedades son necesarias para implementar la [**interfaz IStylesProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider)



| Miembros requeridos                                                            | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Propiedad    | Ninguno  |
| [**FillColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Propiedad    | Ninguno  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Propiedad    | Ninguno  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Propiedad    | Ninguno  |
| [**Forma**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Propiedad    | Ninguno  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Propiedad    | Ninguno  |
| [**NombreEstilo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Propiedad    | Ninguno  |



 

Este patrón de control no tiene métodos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 