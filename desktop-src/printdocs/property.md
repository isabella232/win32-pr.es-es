---
description: Obtenga información sobre el elemento Property en documentos e impresión. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propiedad (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d89913daa9f828fddd4f9fb8dee8bd6a53e01
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883455"
---
# <a name="property-documents-and-printing"></a>Propiedad (documentos e impresión)

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Property declara un dispositivo, un formato de trabajo u otra propiedad pertinente cuyo nombre se proporciona mediante su atributo name. Se usa un elemento Value para asignar un valor a la propiedad .

Una propiedad puede ser compleja, posiblemente que contenga varias subpropiedades. Las subpropiedades también se representan mediante elementos Property.

## <a name="element-tag"></a>Etiqueta de elemento

&lt;Propiedad&gt;

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo name de la propiedad , que es una propiedad estándar o una propiedad definida de forma privada. <br/> |



 

Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | PrintCapabilities <br/> Característica<br/> PrintTicket<br/> Opción<br/> ParameterDef<br/> Propiedad<br/> ScoredProperty<br/>                                                                                                                                                              |
| Elementos secundarios<br/>  | El sistema no asigna ninguna importancia a la ordenación de los elementos. Si los clientes deciden atribuir cierta importancia en el orden de los elementos, pueden hacerlo libremente. <br/> *Valor* de propiedad (uno o *más)* (cero o más)<br/> o <br/> *Valor* de propiedad (cero o *más)* (uno o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> Se permiten elementos value secundarios duplicados que son elementos del mismo nivel.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Una propiedad puede tener dependencias de configuración, excepto cuando aparece dentro de un elemento ParameterDef.

## <a name="element-usage"></a>Uso de elementos

Además de aparecer en los elementos Feature y Option, los elementos Property pueden aparecer en el nivel raíz de las tecnologías subyacentes respectivas. El esquema de impresión define un conjunto de elementos Property que se pueden usar para describir un dispositivo de una manera portátil. Sin embargo, si estas propiedades no son suficientes para sus necesidades como proveedor printCapabilities (normalmente porque el dispositivo que se admite tiene aspectos nuevos no previstos por el esquema de impresión), puede introducir sus propios elementos Property privados. Puede mejorar o elaborar la información proporcionada por una propiedad pública agregando una o varias subpropiedades privadas como contenido de elemento de la propiedad pública.

Los elementos de propiedad se definen mediante una etiqueta de elemento XML, &lt; Property &gt; . A cada propiedad se le asigna un nombre por medio de su atributo name. El nombre debe ser un QName XML y debe cumplir la Convención de espacio de nombres. Para obtener más información, vea [Atributos XML.](xml-attributes.md) El atributo Nombre de propiedad y su ubicación dentro de la jerarquía de elementos Property primarios (si es una subpropiedad) identifican de forma única la propiedad dentro del documento PrintCapabilities o PrintTicket.

Una propiedad puede contener uno o varios elementos Value, uno o varios elementos Property secundarios (denominados subpropiedades) o una combinación de ambos. Las subpropiedades son útiles cuando la propiedad se compone de varios componentes. Por ejemplo, una propiedad "ConsumableColor" podría tener componentes "C", "M" e "Y".

## <a name="example"></a>Ejemplo

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




