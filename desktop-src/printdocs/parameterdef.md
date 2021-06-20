---
description: Obtenga información sobre el elemento ParameterDef, que define las características válidas de la entrada de parámetros. El valor se especifica mediante un elemento ParameterInit.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2682e3da11f471401e95e3f6515de5e18b6be895
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407298"
---
# <a name="parameterdef"></a>ParameterDef

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef define las características válidas de la entrada de parámetros. El valor se especifica mediante un elemento ParameterInit.

## <a name="element-tag"></a>Etiqueta de elemento

<ParameterDef>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Define un nombre único para el parámetro en el contexto del documento actual. Los atributos de nombre ParameterDef duplicados representan el documento PrintCapabilities como no válido.<br/> |



 

Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)

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
<td>PrintCapabilities <br/></td>
</tr>
<tr class="even">
<td>Elementos secundarios<br/></td>
<td>Property (uno o varios)<br/> Los siguientes elementos Property estándar deben aparecer como el contenido de un elemento ParameterDef. <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>Mandatory <br/></li>
<li>MaxLength o MaxValue<br/></li>
<li>MinLength o MinValue<br/></li>
<li>Varios* <br/></li>
<li>UnitType <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Este elemento<br/></td>
<td>No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados del mismo nivel.<br/></td>
</tr>
</tbody>
</table>



 

\*Se requiere cuando DataType es entero o decimal. Opcional cuando DataType es string.

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que parameterdef y su contenido en cualquier nivel de anidamiento no tengan dependencias de configuración.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se establecen todos los elementos Property necesarios para este parámetro. En el ejemplo [de ParameterInit](parameterinit.md) se muestra cómo inicializar este parámetro.

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




