---
description: Obtenga información sobre el elemento JobCopiesAllDocuments, que especifica el número de copias de un trabajo.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597aea94f62ee7ce5b5663a301ce5a1783113baa6f40fcbdf465ec159d72fe61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471698"
---
# <a name="jobcopiesalldocuments"></a>JobCopiesAllDocuments

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el número de copias de un trabajo.

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|-------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/> |
| Prefijo de ámbito <br/> | Trabajo<br/>          |
| Notas <br/>          | Ninguno<br/>         |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es:

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propiedades de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Valor                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | integer<br/> | 1<br/>                 |
| MaxValue<br/>     | integer<br/> | no definido<br/>         |
| MinValue<br/>     | integer<br/> | 1<br/>                 |
| Mandatory<br/>    | string<br/>  | psk:Unconditional<br/> |
| Varios<br/>     | integer<br/> | 1<br/>                 |
| UnitType<br/>     | string<br/>  | Copias<br/>            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




