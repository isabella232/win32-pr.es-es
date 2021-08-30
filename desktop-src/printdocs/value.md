---
description: Obtenga información sobre el elemento Value, que asocia un literal a un tipo. El tipo de datos de Value debe ser cadena, entero, decimal o QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345ef8a40b7c87db68259f2815b07cfda0e5bc57
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885992"
---
# <a name="value"></a>Value

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Value asocia un literal a un tipo.

## <a name="element-tag"></a>Etiqueta de elemento

&lt;Valor&gt;

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML       | Detalles                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Especifica el tipo de datos value, que debe ser uno de los siguientes tipos definidos por XSD: cadena, entero, decimal, QName. Si falta, el tipo de datos predeterminado es string.<br/> |



 

Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | ParameterInit <br/> Propiedad<br/> ScoredProperty<br/>                                                                                   |
| Elementos secundarios<br/>  | Solo se permite el contenido de caracteres o enteros.<br/>                                                                                                |
| Este elemento<br/>    | Se permite el contenido NULL. El contenido de caracteres debe ajustarse a la sintaxis definida por el tipo de datos.<br/> No se permiten elementos secundarios duplicados del mismo nivel.<br/> |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que los elementos de valor que aparecen dentro del elemento ScoredProperty no tengan dependencias de configuración. Los elementos de valor que aparecen dentro de los elementos Property pueden tener dependencias arbitrarias en la configuración.

## <a name="element-usage"></a>Uso de elementos

Un elemento Value puede aparecer dentro de un elemento Property o ScoredProperty. El propósito del elemento Value es representar un valor como un tipo de datos XML estándar. El tipo de datos se especifica como un atributo XML del elemento Value, xsi:type. Tenga en cuenta que no se admiten todos los tipos definidos por XSD o XML. Para obtener una lista de los tipos admitidos, [vea Resumen de tipos de elementos](summary-of-element-types.md). Un elemento Value solo puede contener contenido de caracteres. Nada más puede aparecer como contenido en un elemento Value.

> [!Note]  
> Algunos elementos Print Schema-defined Property y ScoredProperty no contienen un elemento Value, ya que su finalidad es simplemente ser elementos primarios de subpropiedades. No debe agregar un elemento Value a propiedades como estas, propiedades que no contienen un elemento Value.

 

Para ajustarse al marco de esquema de impresión, que requiere que un elemento Value o subelementos esté presente en los elementos que admiten valores, se debe representar un valor ausente o indefinido mediante la presentación del elemento Value como un elemento vacío; es decir, como &lt; Valor &gt; &lt; /Valor &gt; .

## <a name="example"></a>Ejemplo

Defina un valor de tipo decimal e inicialízcalo en "128.5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




