---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6019cd2e4d73e1869f0a71795923509566afebd0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105660023"
---
# <a name="pageblackgenerationprocessing"></a>PageBlackGenerationProcessing

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el comportamiento de generación de negro para las separaciones CMYK.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [Contenido de lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                    |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Característica<br/> |
| Prefijo de ámbito <br/> | Página<br/>    |
| Notas <br/>          | Ninguno <br/>   |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                               | Tipo de datos         | Unidad                  | Valores admitidos                                                                                                                                                                      | Resumen                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caracteres<br/> | Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenido de lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres. El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




