---
description: Este tema no es actual. Para obtener información actual, vea Especificación del esquema de impresión.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Elementos ParameterDef y ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa945ad7fec484828bd81b2052f9b330d0e1679
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475131"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Elementos ParameterDef y ParameterInit

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef difiere de un elemento ParameterInit en que describe el valor que puede contener un elemento ParameterInit, mientras que un elemento ParameterInit asigna un valor al parámetro. Un elemento ParameterDef consta de un conjunto específico de elementos Property, que son elementos secundarios del elemento ParameterDef, que especifican el tipo de datos, los valores máximos, mínimos y predeterminados de los datos, y otra información. Estos elementos Property se de abordan más adelante en este tema.

Los elementos ParameterDef solo pueden aparecer en su contexto permitido. Para la versión inicial del esquema de impresión, pueden encontrarse en el nivel raíz del documento PrintCapabilities. El atributo name del elemento ParameterDef define el nombre del parámetro. A cada elemento ParameterDef del documento PrintCapabilities se le debe asignar un atributo de nombre único.

> [!Note]
> para imprimir funcionalidades Proveedores de documentos:
> 
> El significado de un nombre de parámetro es universal; Es decir, si un elemento ParameterDef de un documento PrintCapabilities tiene el mismo atributo de nombre (la cadena formada a partir del espacio de nombres y el nombre descriptivo del elemento ParameterDef) como elemento ParameterDef en otro documento PrintCapabilities, se supone que ambos elementos representan el mismo concepto y deben interpretarse de la misma manera. Por lo tanto, se puede usar un elemento ParameterDef definido en printTicket para un documento PrintCapabilities para inicializar el elemento ParameterInit del mismo nombre definido en un documento PrintCapabilities diferente.

 

## <a name="relationship-to-xml-attributes"></a>Relación con atributos XML

Como sucede con todos los atributos de nombre, el nombre del parámetro tiene el formato de QName XML. Una construcción de parámetros definida por el esquema tiene un nombre calificado por el espacio de nombres público, que forma el atributo name, mientras que el atributo name de una construcción de parámetros definidos de forma privada está calificado por un espacio de nombres privado que es único para el creador.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relación entre ParameterDef y tipos de elemento property

Los elementos ParameterDef que se definen en las palabras clave de esquema de impresión deben estar totalmente definidos en un documento PrintCapabilities. El documento Palabras clave de esquema de impresión proporciona valores nominales para algunos elementos Property de un elemento ParameterDef (como DefaultValue y otros), pero el autor de un documento PrintCapabilities es responsable de definir los elementos Property restantes. En cualquier caso, todos los elementos Property deben definirse explícitamente en un elemento ParameterDef, incluidos los que se definen en las palabras clave de esquema de impresión.

Determinados elementos Property de cada elemento ParameterDef que aparece en las palabras clave de esquema de impresión se designan *como inmutables.* Esto significa que todas las definiciones de documentos PrintCapabilities de los elementos ParameterDef definidos por palabras clave de esquema de impresión deben conservar estos elementos Property sin modificaciones. Estos elementos Property inmutables permiten que las construcciones de parámetros sean portátiles e inequívocas en todos los documentos PrintCapabilities. Un ejemplo primo son las unidades usadas en un elemento ParameterDef. Estas unidades deben ser inmutables para promover una comprensión coherente de su significado. Los elementos de propiedad de un elemento ParameterDef que se designan como no inmutables se pueden volver a definir dentro de un documento PrintCapabilities.

Un elemento ParameterDef se compone de los siguientes elementos Property. Todos deben estar presentes a menos que se indique lo contrario.




| Nombre de la propiedad | Valores | Descripción | ¿Inmutable? | 
|---------------|--------|-------------|------------|
| DataType <br /> | integer <br /> Decimal<br /> string<br /> Ningún valor predeterminado.<br /> | Especifica si el valor del parámetro es un entero, un número de punto flotante o una cadena de texto. El valor de un parámetro se expresa en el mismo formato que el tipo de datos básico XSD correspondiente; es decir, como un entero, un decimal o una cadena. <br /> | Sí<br /> | 
| DefaultValue <br /> | Tipo especificado por la propiedad DataType.<br /> Ningún valor predeterminado.<br /> | Especifica el valor con el que se va a inicializar un control de interfaz de usuario (UI).<br /><ul><li>o <br /></li></ul>Especifica el valor que se va a usar si falta el elemento de parámetro pertinente en PrintTicket.<br /> | No<br /> | 
| Mandatory <br /> | Incondicional: siempre se debe proporcionar el elemento ParameterInit. <br /> Condicional: el elemento ParameterInit solo es necesario si se hace referencia al parámetro dentro de un elemento Option en printTicket.<br /> DefaultValue: condicional.<br /> | Indica cuándo debe aparecer explícitamente un elemento ParameterInit. Si es Condicional, se debe inicializar ParameterInit si PrintTicket contiene una opción que hace referencia al parámetro .<br /> Usado por los clientes de interfaz de usuario y los proveedores PrintCapabilities o PrintTicket. Tenga en cuenta que, en cualquier restricción, la propiedad Mandatory del elemento ParameterDef debe establecerse en Incondicional. ParameterDef debe tener un valor definido; de lo contrario, no se pudo evaluar el valor o la restricción dependientes.<br /> | No<br /> | 
| MaxLength <br /> | entero si la propiedad DataType especifica la cadena.<br /> DefaultValue: no se aplica ningún valor máximo.<br /> | Para los parámetros con valores de cadena, especifica la cadena permitida más larga. Los proveedores ui y PrintCapabilities o PrintTicket usan esta propiedad para validar el elemento ParameterDef.<br /> | No<br /> | 
| MaxValue <br /> | entero si la propiedad DataType especifica un entero.<br /> decimal si la propiedad DataType especifica decimal.<br /> DefaultValue: no se aplica ningún valor máximo.<br /> | Para los elementos ParameterDef con valores enteros o decimales, define el valor permitido más grande.<br /> | No<br /> | 
| MinLength <br /> | entero si la propiedad DataType especifica la cadena. <br /> DefaultValue: no se aplica ningún valor mínimo.<br /> | Para los valores de cadena, define la cadena permitida más corta. Los proveedores ui y PrintCapabilities o PrintTicket usan esta propiedad para validar el elemento ParameterDef.<br /> | No<br /> | 
| MinValue <br /> | entero si la propiedad DataType especifica un entero.<br /> decimal si la propiedad DataType especifica decimal.<br /> DefaultValue: no se aplica ningún valor mínimo.<br /> | Para los parámetros con valores enteros o decimales, define el valor permitido más pequeño. <br /> | No<br /> | 
| Múltiple <br /> | entero si la propiedad DataType especifica un entero.<br /> decimal si la propiedad DataType especifica decimal.<br /> DefaultValue: 1<br /> | Para los parámetros con valores enteros o decimales, el valor del parámetro debe ser un múltiplo de este número. Para obtener más información, vea <a href="#notes-on-multiple">Notes on Multiple (Notas sobre varios)</a> a continuación de esta tabla.<br /> | No<br /> | 
| UnitType <br /> | Valor de cadena que indica las unidades usadas para el parámetro .<br /> Ningún valor predeterminado.<br /> | Indica las unidades en las que se expresa el parámetro. Por ejemplo, ángulos en décimas de grados, longitudes en micrones, y así sucesivamente.<br /> | Sí<br /> | 




 

## <a name="notes-on-multiple"></a>Notas sobre varios

Para los elementos ParameterInit con valores enteros o decimales, el valor de ParameterInit debe ser un múltiplo de este número. Por ejemplo, los elementos ParameterInit con valores decimales se pueden limitar a décimas estableciendo esta propiedad en 0,1. Los elementos de la interfaz de usuario usan esta propiedad cuando construyen diálogos y controles de interfaz de usuario. Además, el código de validación PrintTicket puede usar esta propiedad para redondear el valor de ParameterInit al valor más cercano indicado por Multiple. Nota: Los controladores de dispositivos y los proveedores de PrintCapabilities no deben suponer que los valores ParameterInit son múltiplo de este valor de propiedad. Cada proveedor debe ser capaz de redondear valores arbitrarios al valor utilizable más cercano debido a la posibilidad de que distintos proveedores puedan especificar valores diferentes y en conflicto para esta propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




