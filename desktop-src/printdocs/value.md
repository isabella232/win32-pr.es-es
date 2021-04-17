---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105653129"
---
# <a name="value"></a>Value

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento de valor asocia un literal a un tipo.

## <a name="element-tag"></a>Etiqueta de elemento

<Value>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML       | Detalles                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Especifica el tipo de datos de Value, que debe ser uno de los siguientes tipos definidos por XSD: String, integer, decimal, QName. Si falta, el tipo de datos predeterminado es String.<br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | ParameterInit <br/> Propiedad<br/> ScoredProperty<br/>                                                                                   |
| Elementos secundarios<br/>  | Solo se permite el contenido de caracteres o enteros.<br/>                                                                                                |
| Este elemento<br/>    | Se permite el contenido null. El contenido de los caracteres debe ajustarse a la sintaxis definida por el tipo de datos.<br/> No se permiten nodos secundarios duplicados.<br/> |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Los elementos de valor que aparecen en el elemento ScoredProperty no pueden tener dependencias de configuración. Los elementos de valor que aparecen dentro de los elementos de propiedad pueden tener dependencias arbitrarias en la configuración.

## <a name="element-usage"></a>Uso de elementos

Un elemento de valor puede aparecer dentro de una propiedad o un elemento ScoredProperty. El propósito del elemento Value es representar un valor como un tipo de datos XML estándar. El tipo de datos se especifica como un atributo XML del elemento Value, xsi: Type. Tenga en cuenta que no se admiten todos los tipos definidos por XSD o definidos por XML. Para obtener una lista de los tipos admitidos, vea [Resumen de tipos de elementos](summary-of-element-types.md). Un elemento de valor solo puede contener contenido de caracteres. Nada más puede aparecer como contenido en un elemento de valor.

> [!Note]  
> Algunos elementos ScoredProperty y de propiedad definidos por el esquema de impresión no contienen un elemento de valor, porque su finalidad es simplemente ser elementos primarios de subpropiedades. No debe agregar un elemento de valor a tales propiedades, como las propiedades que no contienen un elemento de valor.

 

Para cumplir con el marco de trabajo del esquema de impresión, que requiere que haya un elemento de valor o subelementos en los elementos que admiten valores, se debe representar un valor ausente o indefinido presentando el elemento de valor como un elemento vacío. es decir, como <Value></Value>.

## <a name="example"></a>Ejemplo

Defina un valor de tipo decimal e Inicialícelo en "128,5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




