---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 29d7ae65-9dd3-4a29-8e5e-79708638a3bb
title: PageMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8312554d8616ed31ea99cd0cc011b2b549d915f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707652"
---
# <a name="pagemediatype"></a>PageMediaType

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe las opciones de MediaType y las características de cada opción.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [Contenido de lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                    |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Característica<br/> |
| Prefijo de ámbito <br/> | Página<br/>    |
| Notas <br/>          | Ninguno<br/>    |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">_BackCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">_FrontCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_MaterialValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">_PrePrintedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">_PrePunchedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">_RecycledValue_</psf:Value>
    </psf:ScoredProperty>     
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_WeightValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                               | Tipo de datos          | Unidad                              | Valores admitidos                                                                                                                                                                      | Resumen                                                                      |
|------------------------------------|--------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/>  | caracteres<br/>             | Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/>  | N/D<br/>                    | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |
| \_BackCoatingValue\_<br/>    | string<br/>  | N/D<br/>                    | Satinado, HighGloss, mate, ninguno, satinado, semibrillante.<br/>                                                                                                                          | Especifica el revestimiento del lado posterior del elemento multimedia.<br/>              |
| \_FrontCoatingValue\_<br/>   | string<br/>  | N/D<br/>                    | Satinado, HighGloss, mate, ninguno, satinado, semibrillante.<br/>                                                                                                                          | Especifica el revestimiento del lado frontal del medio.<br/>             |
| \_MaterialValue\_<br/>       | string<br/>  | N/D<br/>                    | Aluminio, display, DryFilm, Paper, poliéster, Transparency, WetFilm.<br/>                                                                                                       | Especifica el material del que se extrae el contenido multimedia.<br/>                  |
| \_PrePrintedValue\_<br/>     | string<br/>  | N/D<br/>                    | Ninguno, preimpreso, membrete.<br/>                                                                                                                                              | Especifica características preimpresas de medios.<br/>                       |
| \_PrePunchedValue\_<br/>     | string<br/>  | N/D<br/>                    | Ninguno, preperforado.<br/>                                                                                                                                                          | Especifica características preperforadas de medios.<br/>                       |
| \_RecycledValue\_<br/>       | string<br/>  | N/D<br/>                    | Ninguno, estándar.<br/>                                                                                                                                                            | Especifica las características recicladas de medios.<br/>                         |
| \_WeightValue\_<br/>         | integer<br/> | g por metro cuadrado<br/> | Mayor que 0.<br/>                                                                                                                                                            | Especifica las características del peso del medio.<br/>                           |



 

## <a name="extensible-markup-language-xml-content"></a>Contenido de lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` espacio de nombres. El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies Media would be Automatically selected. -->
  <psf:Option name="psk:AutoSelect"/>
  <!-- Specifies archival quality media. -->
  <psf:Option name="psk:Archival">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty back printing film media. -->
  <psf:Option name="psk:BackPrintFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard bond media. -->
  <psf:Option name="psk:Bond">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard card stock media. -->
  <psf:Option name="psk:CardStock">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies continuous feed media. -->
  <psf:Option name="psk:Continous">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard envelope media. -->
  <psf:Option name="psk:EnvelopePlain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies windowed envelope media. -->
  <psf:Option name="psk:EnvelopeWindow">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies fabric media. -->
  <psf:Option name="psk:Fabric">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Polyester</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty high resolution media. -->
  <psf:Option name="psk:HighResolution">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies label media. -->
  <psf:Option name="psk:Label">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies attached multi-part forms media. -->
  <psf:Option name="psk:MultiLayerForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies separate multi-part forms media. -->
  <psf:Option name="psk:MultiPartForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard photographic media. -->
  <psf:Option name="psk:Photographic">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies film photographic media. -->
  <psf:Option name="psk:PhotographicFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies glossy photographic media. -->
  <psf:Option name="psk:PhotographicGlossy">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Glossy</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies high gloss photographic media. -->
  <psf:Option name="psk:PhotographicHighGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">HighGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies matte photographic media. -->
  <psf:Option name="psk:PhotographicMatte">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Matte</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies satin photographic media. -->
  <psf:Option name="psk:PhotographicSatin">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Satin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies semi-gloss photographic media. -->
  <psf:Option name="psk:PhotographicSemiGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">SemiGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard paper media. -->
  <psf:Option name="psk:Plain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in continuous form. -->
  <psf:Option name="psk:Screen">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in paged form. -->
  <psf:Option name="psk:ScreenPaged">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty stationery media. -->
  <psf:Option name="psk:Stationery">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">Letterhead</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is not pre-cut (single tabs). -->
  <psf:Option name="psk:TabStockFull">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is pre-cut (multiple tabs). -->
  <psf:Option name="psk:TabStockPreCut">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies transparency media. -->
  <psf:Option name="psk:Transparency">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Transparency</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty T-shirt transfer media. -->
  <psf:Option name="psk:TShirtTransfer">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies unknown or unlisted media. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
