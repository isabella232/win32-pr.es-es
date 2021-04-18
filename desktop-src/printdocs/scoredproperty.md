---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721391"
---
# <a name="scoredproperty"></a>ScoredProperty

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ScoredProperty declara una propiedad que es intrínseca a una definición de opción. Estas propiedades se deben comparar al evaluar el grado en que una opción solicitada coincide con una opción admitida por el dispositivo.

## <a name="element-tag"></a>Etiqueta de elemento

<ScoredProperty>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo de nombre del ScoredProperty, ya sea una propiedad estándar o una propiedad definida de forma privada. <br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | *Opción*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Elementos secundarios<br/>  | Es posible usar el<br/> *ParameterRef* (uno)<br/> or<br/> *Valor* (uno)<br/> *Propiedad* (cero o más)<br/> *ScoredProperty* (cero o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten nodos secundarios duplicados.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Un elemento ScoredProperty no puede tener dependencias de configuración.

## <a name="example"></a>Ejemplo

Declare un elemento ScoredProperty denominado MediaSizeWidth con un valor de 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




