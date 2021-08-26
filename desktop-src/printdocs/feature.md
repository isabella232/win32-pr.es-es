---
description: Revise elementos Feature, que contienen una lista de elementos Option y Property que describen un atributo de dispositivo, una configuración de formato de trabajo u otra característica pertinente.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Característica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d35686674d08ea0ea4030648b06803919e5d07
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882494"
---
# <a name="feature"></a>Característica

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Feature contiene una lista completa de los elementos Option y Property que describen completamente un atributo de dispositivo, una configuración de formato de trabajo u otra característica pertinente.

## <a name="element-tag"></a>Etiqueta de elemento

&lt;Característica&gt;

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el nombre de la característica, ya sea una característica estándar o una característica definida de forma privada. <br/> |



 

Para más información, consulte la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.




| Category | Detalles | 
|----------|---------|
| Elementos primarios<br /> | PrintCapabilities <br /> PrintTicket <br /> Característica<br /> | 
| Elementos secundarios<br /> | Uno de los grupos siguientes:<br /><ul><li><em>Característica</em> (cero o más)<br /></li><li><em>Opción</em> (uno o varios)<br /></li><li><em>Propiedad</em> (cero o más)<br /></li></ul>o <br /><ul><li><em>Característica</em> (uno o varios)<br /></li><li><em>Opción</em> (cero o más)<br /></li><li><em>Propiedad</em> (cero o más)<br /></li></ul> | 
| Este elemento<br /> | No se permiten datos de caracteres.<br /> Se permiten elementos secundarios duplicados de la opción que son elementos del mismo nivel. Se permiten métodos abreviados de atributo de nombre duplicados. <br /> | 




 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que los elementos de características no tengan dependencias de configuración.

## <a name="element-usage"></a>Uso de elementos

### <a name="relationship-to-xml-attributes"></a>Relación con atributos XML

En la representación Característica/Opción, un atributo de dispositivo se representa mediante un elemento Feature. El atributo device se identifica de forma única mediante el atributo name en el elemento Feature del atributo de dispositivo, como en el ejemplo siguiente. En este ejemplo, el atributo de dispositivo es Resolución.

``` syntax
<Feature name="Resolution" />
```

El esquema de impresión define un conjunto de atributos de nombre para determinadas instancias de característica. Estos atributos de nombre sirven para identificar un conjunto de instancias de características predefinidas asociadas a atributos de dispositivo configurables específicos. Estos nombres de instancia de características se deben usar siempre que corresponda, ya que aumentan la portabilidad del documento PrintCapabilities y los PrintTickets que se derivan de ellos. Se pueden introducir instancias de características definidas de forma privada si determinados atributos de dispositivo no se corresponden con ninguna de las instancias de características definidas por el esquema. Para obtener información sobre la sintaxis de los atributos de nombre y las convenciones que se aplican a los nombres definidos por el esquema y definidos de forma privada, vea [Atributos XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Elemento Relationship to Option

Cada uno de los estados posibles se representa mediante un elemento Option. Cada definición de opción contiene uno o varios elementos ScoredProperty, que juntos describen o caracterizan de forma única el estado que se representa. La técnica utilizada para crear definiciones de opción se describe en [Definiciones de opciones](option-definitions.md). Todos los elementos Option asociados a un elemento Feature determinado residen como elementos secundarios del elemento Feature.

### <a name="subfeatures"></a>Subfunciones

El marco de trabajo de esquema de impresión también permite agrupar los elementos feature de forma jerárquica. Es decir, un elemento Feature puede contener uno o varios elementos secundarios (subatures). Esto puede ser útil para organizar elementos feature relacionados o para elementos Feature que controlan aspectos de una característica de dispositivo. Un ejemplo es un dispositivo que admite el stapling. Este tipo de dispositivo puede ofrecer al usuario la opción de dónde buscar el grapa, como en la esquina superior izquierda, en la esquina superior derecha, en el borde superior o en el borde izquierdo. La interfaz de usuario (UI) de este dispositivo debe ser capaz de presentar primero al usuario las opciones de nivel más alto, que en este caso es si se va a usar el estapling. Solo después de que el usuario haya decidido usar el stapling en caso de que se le presente un segundo nivel de opciones, la ubicación de la grapa. Una jerarquía de características agrega la estructura adicional que hace posible este tipo de interfaz de usuario. Print Schema Framework permite que las subaturísticas tengan sus propias subatures secundarias, lo que permite un nivel ilimitado de anidamiento.

El marco de trabajo de esquema de impresión también permite que los elementos Option aparezcan en el mismo nivel que las subatures; es decir, como elementos del mismo nivel dentro del mismo elemento principal feature. Esto permite al usuario tomar la decisión de alto nivel (si se debe usar el stapling) antes de realizar las selecciones de subfeature. En este ejemplo, el elemento raíz Feature, "Grapa", podría contener dos elementos Option, "On" y "Off", así como una subfeature denominada "ElementLocation".

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

 

 




