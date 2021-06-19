---
description: Obtenga más información sobre el parámetro PageWatermarkTextText. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395970"
---
# <a name="pagewatermarktexttext"></a>PageWatermarkTextText

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el texto de la marca de agua.

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|--------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                    |
| Prefijo de ámbito <br/> | Página<br/>                            |
| Notas <br/>          | Vinculado al elemento PageWatermark<br/> |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es la siguiente:

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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
| DataType<br/>     | String<br/>  | xs:string<br/>       |
| DefaultValue<br/> | Entero<br/> | no definido<br/>       |
| MaxLength<br/>    | Entero<br/> | no definido<br/>       |
| MinLength<br/>    | Entero<br/> | 1<br/>               |
| Mandatory<br/>    | String<br/>  | psk:Conditional<br/> |
| UnitType<br/>     | String<br/>  | caracteres<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




