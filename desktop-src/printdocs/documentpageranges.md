---
description: Obtenga información sobre el elemento DocumentPageRanges, que describe el intervalo de salida del documento en páginas.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409258"
---
# <a name="documentpageranges"></a>DocumentPageRanges

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe el intervalo de salida del documento en páginas. El valor del parámetro debe ajustarse a la estructura siguiente:

-   PageRangeText: "*PageRange*" o "*PageRange*,*PageRange*"

-   PageRange: "*PageNumber*" o "*PageNumber* - *PageNumber*"

-   PageNumber: de 1 a N, donde N es el número de páginas del documento. Si *PageNumber* > N, *PageNumber* = N.

Se debe omitir el espacio en blanco de la cadena.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|-------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/> |
| Prefijo de ámbito <br/> | Documento<br/>     |
| Notas <br/>          | Ninguno<br/>         |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propiedades de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Valor                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | no definido<br/>       |
| MaxLength<br/>    | integer<br/> | no definido<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Mandatory<br/>    | string<br/>  | psk:Conditional<br/> |
| UnitType<br/>     | string<br/>  | caracteres<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




