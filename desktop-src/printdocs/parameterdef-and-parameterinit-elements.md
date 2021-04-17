---
description: Este tema no está actualizado. Para obtener información actual, consulte la especificación del esquema de impresión.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Elementos ParameterDef y ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698005"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Elementos ParameterDef y ParameterInit

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef difiere de un elemento ParameterInit en que describe el valor que puede contener un elemento ParameterInit, mientras que un elemento ParameterInit asigna un valor al parámetro. Un elemento ParameterDef está compuesto de un conjunto específico de elementos de propiedad, que son elementos secundarios del elemento ParameterDef, que especifican el tipo de datos, el máximo, el mínimo y los valores predeterminados para los datos, y otra información. Estos elementos de propiedad se describen más adelante en este tema.

Los elementos ParameterDef solo pueden aparecer en su contexto permitido. En la versión inicial del esquema de impresión, pueden encontrarse en el nivel raíz del documento de PrintCapabilities. El atributo name del elemento ParameterDef define el nombre del parámetro. Cada elemento ParameterDef del documento PrintCapabilities debe tener asignado un atributo de nombre único.

> [!Note]
> para imprimir proveedores de documentos de funcionalidades:
> 
> El significado de un nombre de parámetro es universal; es decir, si un elemento ParameterDef de un documento de PrintCapabilities tiene el mismo atributo de nombre (la cadena formada a partir del espacio de nombres y el nombre descriptivo del elemento ParameterDef) como un elemento ParameterDef en otro documento de PrintCapabilities, se supone que ambos elementos representan el mismo concepto y deben interpretarse de la misma manera. Por lo tanto, se puede usar un elemento ParameterDef definido en un PrintTicket para un documento PrintCapabilities para inicializar el elemento ParameterInit del mismo nombre definido en un documento PrintCapabilities diferente.

 

## <a name="relationship-to-xml-attributes"></a>Relación con atributos XML

Como ocurre con todos los atributos de nombre, el nombre del parámetro tiene el formato de un QName XML. Una construcción de parámetro definida por el esquema tiene un nombre que está calificado por el espacio de nombres público, formando el atributo de nombre, mientras que el atributo de nombre de una construcción de parámetro definida de forma privada está calificado por un espacio de nombres privado que es único para el creador.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relación entre los tipos de elemento de propiedad y ParameterDef

Los elementos ParameterDef que se definen en las palabras clave del esquema de impresión deben estar totalmente definidos en un documento de PrintCapabilities. El documento imprimir palabras clave del esquema proporciona valores nominales para algunos elementos de propiedad de un elemento ParameterDef (como DefaultValue y otros), pero el autor de un documento PrintCapabilities es responsable de definir los elementos de propiedad restantes. En cualquier caso, todos los elementos de propiedad deben definirse explícitamente en un elemento ParameterDef, incluidos los que están definidos en las palabras clave del esquema de impresión.

Algunos elementos de propiedad de cada elemento ParameterDef que aparecen en las palabras clave del esquema de impresión se designan como *inmutables*. Esto significa que todas las definiciones de documentos de PrintCapabilities de los elementos ParameterDef definidos por palabras clave del esquema Print deben conservar estos elementos de propiedad sin modificarlos. Estos elementos de propiedad inmutables permiten a las construcciones de parámetros ser portátiles e inequívocas en todos los documentos de PrintCapabilities. Un ejemplo primo son las unidades utilizadas en un elemento ParameterDef. Estas unidades deben ser inmutables para promover una comprensión coherente de su significado. Los elementos de propiedad de un ParameterDef que se designan como no inmutables se pueden redefinir dentro de un documento de PrintCapabilities.

Un elemento ParameterDef se compone de los siguientes elementos Property. Todo debe estar presente a menos que se indique lo contrario.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre de la propiedad</th>
<th>Valores</th>
<th>Descripción</th>
<th>Inmutable?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataType <br/></td>
<td>integer <br/> Decimal<br/> string<br/> Ningún valor predeterminado.<br/></td>
<td>Especifica si el valor del parámetro es un entero, un número de punto flotante o una cadena de texto. El valor de un parámetro se expresa en el mismo formato que el tipo de datos XSD Basic correspondiente; es decir, como entero, decimal o cadena. <br/></td>
<td>Sí<br/></td>
</tr>
<tr class="even">
<td>DefaultValue <br/></td>
<td>Tipo especificado por la propiedad DataType.<br/> Ningún valor predeterminado.<br/></td>
<td>Especifica el valor con el que se va a inicializar un control de interfaz de usuario (IU).<br/>
<ul>
<li>or <br/></li>
</ul>
Especifica el valor que se va a usar si falta el elemento de parámetro correspondiente del PrintTicket.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>Mandatory <br/></td>
<td>Incondicional: siempre se debe proporcionar el elemento ParameterInit. <br/> Condicional: el elemento ParameterInit solo es necesario si se hace referencia al parámetro dentro de un elemento Option en PrintTicket.<br/> DefaultValue: condicional.<br/></td>
<td>Indica cuándo debe aparecer explícitamente un elemento ParameterInit. Si es condicional, se debe inicializar ParameterInit si el PrintTicket contiene una opción que hace referencia al parámetro.<br/> Lo usan los clientes de interfaz de usuario y los proveedores de PrintCapabilities o PrintTicket. Tenga en cuenta que, en cualquier restricción, la propiedad obligatoria del elemento ParameterDef debe establecerse en incondicional. ParameterDef debe tener un valor definido; de lo contrario, no se puede evaluar el valor dependiente o la restricción.<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MaxLength <br/></td>
<td>entero si la propiedad DataType especifica una cadena.<br/> DefaultValue: no se aplica ningún valor máximo.<br/></td>
<td>En el caso de los parámetros con valores de cadena, especifica la cadena más larga permitida. Los proveedores de UI y PrintCapabilities o PrintTicket usan esta propiedad para validar el elemento ParameterDef.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MaxValue <br/></td>
<td>entero si la propiedad DataType especifica un entero.<br/> decimal si la propiedad DataType especifica decimal.<br/> DefaultValue: no se aplica ningún valor máximo.<br/></td>
<td>Para los elementos ParameterDef con valores enteros o decimales, define el mayor valor permitido.<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MinLength <br/></td>
<td>entero si la propiedad DataType especifica una cadena. <br/> DefaultValue: no se aplica ningún valor mínimo.<br/></td>
<td>Para los valores de cadena, define la cadena más corta permitida. Los proveedores de UI y PrintCapabilities o PrintTicket usan esta propiedad para validar el elemento ParameterDef.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MinValue <br/></td>
<td>entero si la propiedad DataType especifica un entero.<br/> decimal si la propiedad DataType especifica decimal.<br/> DefaultValue: no se aplica ningún valor mínimo.<br/></td>
<td>En el caso de los parámetros de valores enteros o decimales, define el menor valor permitido. <br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>Múltiple <br/></td>
<td>entero si la propiedad DataType especifica un entero.<br/> decimal si la propiedad DataType especifica decimal.<br/> DefaultValue: 1<br/></td>
<td>En el caso de los parámetros de valores enteros o decimales, el valor del parámetro debe ser un múltiplo de este número. Para obtener más información, vea las <a href="#notes-on-multiple">notas sobre varias</a> siguientes tablas.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>UnitType <br/></td>
<td>valor de cadena que indica las unidades utilizadas para el parámetro.<br/> Ningún valor predeterminado.<br/></td>
<td>Indica las unidades en las que se expresa el parámetro. Por ejemplo, ángulos en décimas de grado, longitudes en microns, etc.<br/></td>
<td>Sí<br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a>Notas en varios

En el caso de los elementos ParameterInit con valores enteros o decimales, el valor de ParameterInit debe ser un múltiplo de este número. Por ejemplo, los elementos ParameterInit con valores decimales se pueden limitar a décimas de valor estableciendo esta propiedad en 0,1. Los elementos de la interfaz de usuario usan esta propiedad cuando crean cuadros de diálogo y controles de interfaz de usuario. Además, el código de validación de PrintTicket puede usar esta propiedad para redondear el valor de ParameterInit al valor más próximo indicado por múltiples. Nota: los controladores de dispositivos y los proveedores de PrintCapabilities no deben suponer que los valores de ParameterInit son múltiplos de este valor de propiedad. Cada proveedor debe ser capaz de redondear valores arbitrarios al valor utilizable más cercano debido a la posibilidad de que varios proveedores puedan especificar valores diferentes y conflictivos para esta propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




