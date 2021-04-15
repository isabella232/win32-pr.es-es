---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propiedad (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361972"
---
# <a name="property-documents-and-printing"></a>Propiedad (documentos e impresión)

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Property declara un dispositivo, un formato de trabajo u otra propiedad pertinente cuyo nombre se proporciona mediante su atributo name. Un elemento Value se utiliza para asignar un valor a la propiedad.

Una propiedad puede ser compleja, posiblemente con varias subpropiedades. Las subpropiedades también se representan mediante elementos de propiedad.

## <a name="element-tag"></a>Etiqueta de elemento

<Property>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo de nombre de la propiedad, que es una propiedad estándar o una propiedad definida de forma privada. <br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | PrintCapabilities <br/> Característica<br/> PrintTicket<br/> Opción<br/> ParameterDef<br/> Propiedad<br/> ScoredProperty<br/>                                                                                                                                                              |
| Elementos secundarios<br/>  | El sistema no asigna importancia al orden de los elementos. Si los clientes optan por tener alguna importancia en el orden de los elementos, pueden hacerlo de forma gratuita. <br/> *Propiedad* (uno o varios *valores* ) (cero o más)<br/> or <br/> *Propiedad* (cero o más) *valor* (uno o varios)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> Se permiten elementos de valor secundario duplicados que son del mismo nivel.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Una propiedad puede tener dependencias de configuración, excepto cuando aparece dentro de un elemento ParameterDef.

## <a name="element-usage"></a>Uso de elementos

Además de aparecer en elementos de características y opciones, los elementos de propiedad pueden aparecer en el nivel raíz de las tecnologías subyacentes respectivas. El esquema de impresión define un conjunto de elementos de propiedad que se pueden usar para describir un dispositivo de manera portátil. Sin embargo, si estas propiedades no son suficientes para sus necesidades como un proveedor de PrintCapabilities (normalmente porque el dispositivo que se está admitiendo tiene aspectos nuevos no previstos por el esquema de impresión), puede introducir sus propios elementos de propiedad privados. Puede mejorar o elaborar la información proporcionada por una propiedad pública agregando una o más subpropiedades privadas como contenido del elemento de la propiedad pública.

Los elementos de propiedad se definen mediante una etiqueta de elemento XML, <Property> . A cada propiedad se le asigna un nombre por medio de su atributo name. El nombre debe ser un QName XML y debe ajustarse a la Convención de espacio de nombres. Para obtener más información, consulte [atributos XML](xml-attributes.md). El atributo de nombre de propiedad y su ubicación dentro de la jerarquía de elementos de propiedad primarios (si es una subpropiedad) identifican de forma única la propiedad dentro del documento PrintCapabilities o PrintTicket.

Una propiedad puede contener uno o más elementos de valor, o uno o varios elementos de propiedad secundarios (denominados subpropiedades) o una combinación de ambos. Las subpropiedades son útiles cuando la propiedad se compone de varios componentes. Por ejemplo, una propiedad "ConsumableColor" podría tener los componentes "C", "M" y "Y".

## <a name="example"></a>Ejemplo

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




