---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998382"
---
# <a name="jobbindalldocumentsgutter"></a>JobBindAllDocumentsGutter

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el ancho del medianía de enlace.

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Value |
|----------------------------|-----------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                 |
| Prefijo de ámbito <br/> | Trabajo <br/>                         |
| Notas <br/>          | Vinculado al elemento JobBinding<br/> |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es:

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propiedades de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Value                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | integer<br/> | no definido<br/>       |
| MaxValue<br/>     | integer<br/> | no definido<br/>       |
| MinValue<br/>     | integer<br/> | no definido<br/>       |
| Mandatory<br/>    | String<br/>  | psk:Conditional<br/> |
| Múltiple<br/>     | integer<br/> | 1<br/>               |
| UnitType<br/>     | string<br/>  | Micras<br/>         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




