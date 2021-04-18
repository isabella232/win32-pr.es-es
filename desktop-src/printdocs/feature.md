---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Característica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707612"
---
# <a name="feature"></a>Característica

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento de característica contiene una lista completa de los elementos de propiedad y opción que describen completamente un atributo de dispositivo, la configuración de formato del trabajo u otras características relevantes.

## <a name="element-tag"></a>Etiqueta de elemento

<Feature>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el nombre de la característica, ya sea una característica estándar o una característica definida de forma privada. <br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Elementos primarios<br/></td>
<td>PrintCapabilities <br/> PrintTicket <br/> Característica<br/></td>
</tr>
<tr class="even">
<td>Elementos secundarios<br/></td>
<td>Uno de los siguientes grupos:<br/>
<ul>
<li><em>Característica</em> (cero o más)<br/></li>
<li><em>Opción</em> (uno o varios)<br/></li>
<li><em>Propiedad</em> (cero o más)<br/></li>
</ul>
or <br/>
<ul>
<li><em>Característica</em> (uno o más)<br/></li>
<li><em>Opción</em> (cero o más)<br/></li>
<li><em>Propiedad</em> (cero o más)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Este elemento<br/></td>
<td>No se permiten datos de caracteres.<br/> Se permiten los elementos de opción secundarios duplicados que son del mismo nivel. Se permiten los métodos abreviados de atributo de nombre duplicados. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que los elementos de característica no tengan dependencias de configuración.

## <a name="element-usage"></a>Uso de elementos

### <a name="relationship-to-xml-attributes"></a>Relación con atributos XML

En la representación de características y opciones, un atributo de dispositivo se representa mediante un elemento de característica. El atributo de dispositivo se identifica de forma única mediante el atributo de nombre en el elemento de característica del atributo de dispositivo, como en el ejemplo siguiente. En este ejemplo, el atributo de dispositivo es resolución.

``` syntax
<Feature name="Resolution" />
```

El esquema de impresión define un conjunto de atributos de nombre para determinadas instancias de características. Estos atributos de nombre sirven para identificar un conjunto de instancias de características predefinidas asociadas a atributos de dispositivo configurables concretos. Estos nombres de instancia de características deben usarse siempre que proceda, ya que aumentan la portabilidad del documento de PrintCapabilities y los elementos PrintTicket derivados de ellos. Es posible que se introduzcan instancias de características definidas de forma privada si determinados atributos de dispositivo no corresponden a ninguna de las instancias de características definidas por el esquema. Para obtener información sobre la sintaxis de los atributos name y las convenciones que se aplican a los nombres definidos por el esquema y los definidos por el personal, vea [atributos XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Relación con el elemento OPTION

Cada uno de los Estados posibles se representa mediante un elemento OPTION. Cada definición de opción contiene uno o más elementos ScoredProperty, que se han tomado juntos de forma única o caracterizan el estado que se está representando. La técnica que se usa para crear definiciones de opciones se describe en [definiciones de opciones](option-definitions.md). Todos los elementos Option asociados a un elemento Feature determinado residen como elementos secundarios del elemento Feature.

### <a name="subfeatures"></a>Subcaracterísticas

El marco de trabajo del esquema de impresión también permite agrupar elementos de características de forma jerárquica. Es decir, un elemento de característica puede contener uno o más elementos de característica secundarios (subcaracterísticas). Esto puede ser útil para organizar elementos de características relacionados o para elementos de características que controlan aspectos de una característica de dispositivo. Un ejemplo es un dispositivo que admite grapado. Este dispositivo podría ofrecer al usuario una opción para ubicar la grapa, como en la esquina superior izquierda o en la esquina superior derecha, o a lo largo del borde superior, o a lo largo del borde izquierdo. La interfaz de usuario (UI) de este dispositivo debe ser capaz de presentar al usuario las opciones de nivel más alto en primer lugar, que en este caso es si se debe usar el grapado. Solo después de que el usuario haya decidido usar el grapado, debe encontrarse con un segundo nivel de opciones, grapar ubicación. Una jerarquía de características agrega la estructura adicional que hace posible la interfaz de usuario. El marco de trabajo de esquema de impresión permite que las subcaracterísticas tengan sus propias subcaracterísticas secundarias, lo que permite un nivel ilimitado de anidamiento.

El marco de trabajo de esquema de impresión también permite que los elementos de opción aparezcan en el mismo nivel que las subcaracterísticas; es decir, como elementos del mismo nivel dentro del mismo elemento de la característica primaria. Esto permite al usuario tomar la decisión de alto nivel (si se va a usar el grapado) antes de realizar las selecciones de subcaracterísticas. En este ejemplo, el elemento de característica raíz, "Grapate", puede contener dos elementos Option, "ON" y "OFF", así como una subcaracterística denominada "StapleLocation".

## <a name="example"></a>Ejemplo

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




