---
description: Obtenga información sobre el parámetro PageMediaSizePSWidthOffset. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549113"
---
# <a name="pagemediasizepswidthoffset"></a>PageMediaSizePSWidthOffset

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el desplazamiento hasta la dirección de orientación de la fuente (Referencia [PostScript especificación de formato de archivo de](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)descripción de impresora ).

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|-------------------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                                     |
| Prefijo de ámbito <br/> | Página<br/>                                             |
| Notas <br/>          | Vinculado al elemento PageMediaSize, opción CustomPS<br/> |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es:

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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



| Propiedad                | xsi:type           | Valor                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | integer<br/> | no definido<br/>       |
| MaxValue<br/>     | integer<br/> | no definido<br/>       |
| MinValue<br/>     | integer<br/> | no definido<br/>       |
| Mandatory<br/>    | string<br/>  | psk:Conditional<br/> |
| Múltiple<br/>     | integer<br/> | 1<br/>               |
| UnitType<br/>     | string<br/>  | Micras<br/>         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[PostScript Especificación de formato de archivo de descripción de impresora](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




