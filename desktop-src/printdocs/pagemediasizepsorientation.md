---
description: Obtenga información sobre el parámetro PageMediaSizePSOrientation. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1b3aff1099199a98d6c8be899824dd1a1f17c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395730"
---
# <a name="pagemediasizepsorientation"></a>PageMediaSizePSOrientation

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica la orientación relativa a la dirección de orientación de la fuente (Especificación de formato de archivo de descripción de impresora [PostScript de referencia).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)

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
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propiedades de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Valor                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | integer<br/> | 0<br/>                 |
| MaxValue<br/>     | integer<br/> | 3<br/>                 |
| MinValue<br/>     | integer<br/> | 0<br/>                 |
| Mandatory<br/>    | string<br/>  | psk:Conditional<br/>   |
| Múltiple<br/>     | integer<br/> | 1<br/>                 |
| UnitType<br/>     | string<br/>  | PageMediaSizeEnum<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de formato de archivo de descripción de impresora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




