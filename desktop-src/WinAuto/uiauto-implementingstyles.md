---
title: Styles (patrón de control)
description: Describe las directrices y convenciones para implementar IStylesProvider, incluida información sobre propiedades y métodos. El patrón de control de estilos se usa para describir un elemento de la interfaz de usuario que tiene un estilo, color de relleno, patrón de relleno o forma específicos.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control de estilos
- Automatización de la interfaz de usuario, patrón de control Styles
- Automatización de la interfaz de usuario, IStylesProvider
- IStylesProvider
- implementar el patrón de control de estilos de UI Automation
- Styles (patrón de control)
- patrones de control, IStylesProvider
- patrones de control, implementar estilos de automatización de la interfaz de usuario
- patrones de control, estilos
- interfaces, IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793353"
---
# <a name="styles-control-pattern"></a>Styles (patrón de control)

Describe las directrices y convenciones para implementar [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), incluida información sobre propiedades y métodos. El patrón de control de **estilos** se usa para describir un elemento de la interfaz de usuario que tiene un estilo, color de relleno, patrón de relleno o forma específicos.

El patrón de control de **estilos** es especialmente útil para describir los elementos de un documento, que suelen tener tales estilos. Los estilos suelen llevar información útil para los clientes con discapacidades. por ejemplo, un estilo puede describir una cadena determinada como título de un documento o un objeto de diagrama de flujo determinado como un rombo o un círculo. Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IStylesProvider**](#required-members-for-istylesprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **styles** , tenga en cuenta las siguientes directrices y convenciones:

-   El archivo de encabezado UIAutomationClient. h define un conjunto de valores constantes con nombre que se utilizan para identificar varios estilos comunes. Para obtener más información, vea [**identificadores de estilo**](uiauto-style-identifiers.md).
-   Si usa el [**StyleId \_ personalizado**](uiauto-style-identifiers.md), debe implementar la propiedad [**IStylesProvider:: StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que los clientes detecten el nombre del estilo. No es necesario implementar la propiedad **StyleName** para un estilo estándar porque la automatización de la interfaz de usuario de Microsoft proporciona un nombre predeterminado, pero se puede implementar si es necesario reemplazar el nombre predeterminado.
-   Las demás propiedades del patrón de **estilos** son opcionales. el proveedor puede devolver [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) para una propiedad que no se admite.
-   Los estilos de un intervalo de texto se pueden representar mediante los siguientes atributos de texto:
    -   Al responder a una solicitud para el atributo de texto [**StyleId**](uiauto-textattribute-ids.md) , el intervalo de texto debe devolver uno de los identificadores de estilo descritos en [**identificadores de estilo**](uiauto-style-identifiers.md).
    -   Si se usa [**StyleId \_ Custom**](uiauto-style-identifiers.md) , el intervalo de texto debe devolver un valor de cadena para el atributo de texto [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) para permitir que los clientes detecten el nombre de estilo.
    -   Un intervalo de texto que tiene varios estilos, como el encabezado y el texto normal, debe devolver la propiedad [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) de automatización de la interfaz de usuario especial para las propiedades [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) y [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) . Un cliente que recibe esta respuesta puede subdividir el intervalo de texto para encontrar dónde comienzan y terminan los estilos.
-   Las aplicaciones pueden usar una amplia variedad de estilos para describir objetos, pero la automatización de la interfaz de usuario solo representa los más comunes. Para representar atributos de estilo adicionales, como el color del borde, un proveedor puede devolver una lista de atributos adicionales en la propiedad [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) . Se trata básicamente de un contenedor de propiedades con un conjunto de propiedades extendidas, como "BorderColor = 0xFF0000;" BorderStyle = punteado ". Los valores de las propiedades extendidas pueden ser específicos de la aplicación.

## <a name="required-members-for-istylesprovider"></a>Miembros requeridos para **IStylesProvider**

Las siguientes propiedades son necesarias para implementar la interfaz [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) .



| Miembros requeridos                                                            | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Propiedad    | None  |
| [**Relleno**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Propiedad    | None  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Propiedad    | None  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Propiedad    | None  |
| [**Forma**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Propiedad    | None  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Propiedad    | None  |
| [**NombreEstilo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Propiedad    | None  |



 

Este patrón de control no tiene métodos o propiedades asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 