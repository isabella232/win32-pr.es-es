---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157cea832015c0dfb208e3f89b31ec19ac2c4313
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717423"
---
# <a name="documentbannersheetsource"></a>DocumentBannerSheetSource

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el origen de una hoja de pancarta personalizada.

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                                                  |
|----------------------------|--------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                          |
| Prefijo de ámbito <br/> | Documento<br/>                              |
| Notas <br/>          | Vinculado al elemento DocumentBannerSheet<br/> |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es:

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
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

## <a name="structure-properties"></a>Propiedades de la estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Value                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | no definido<br/>       |
| MaxLength<br/>    | integer<br/> | no definido<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Mandatory<br/>    | string<br/>  | PSK: condicional<br/> |
| UnitType<br/>     | string<br/>  | caracteres<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




