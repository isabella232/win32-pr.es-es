---
description: Obtenga información sobre el elemento JobOutputBin, que describe la ubicación de salida instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408858"
---
# <a name="joboutputbin"></a>JobOutputBin

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe la ubicación de salida instalada en un dispositivo o la lista completa de ubicaciones admitidas para un dispositivo. Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin son mutuamente excluyentes solo se debe especificar una en un documento PrintTicket o Capacidades de impresión.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [lenguaje de marcado extensible (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Característica<br/> |
| Prefijo de ámbito <br/> | Trabajo<br/>     |
| Notas <br/>          | Ninguno<br/>    |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                                   | Tipo de datos          | Unidad                  | Valores admitidos                                                                                                                                                                      | Resumen                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| \_OptionName\_<br/>              | string<br/>  | caracteres<br/> | Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                  |
| \_IdentityOptionValue\_<br/>     | string<br/>  | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/>        |
| \_BinTypeValue\_<br/>            | string<br/>  | N/D<br/>        | MailBox, Sorter, Stacker, Finisher, None.<br/>                                                                                                                                  | Especifica el tipo general de la ubicación.<br/>                                   |
| \_MediaSheetCapacityValue\_<br/> | integer<br/> | Hojas<br/>     | Restricción de entero máxima permitida por el dispositivo.<br/>                                                                                                                              | Especifica la capacidad multimedia en número de páginas (nivel completo) de la ubicación.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




