---
description: Obtenga información sobre el elemento DocumentDuplex, que describe las características dúplex de la salida. La característica dúplex permite imprimir en ambos lados del medio.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2face0a337bb1f5b2f6f6bd1de8ef0281869a3fcaba0ac4080c0b81f79fedf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939075"
---
# <a name="documentduplex"></a>DocumentDuplex

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe las características dúplex de la salida. La característica dúplex permite imprimir en ambos lados del medio. Cada documento se dúplex por separado. DocumentDuplex y JobDuplexAllDocumentsContiguously son mutuamente excluyentes. Es el controlador quien determina el control de restricciones entre estas palabras clave.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [contenido lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Value |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Característica<br/>  |
| Prefijo de ámbito <br/> | Documento<br/> |
| Notas <br/>          | Ninguno<br/>     |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es la siguiente:

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                               | Tipo de datos         | Unidad                  | Valores admitidos                                                                                                                                                                      | Resumen                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caracteres<br/> | Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                                                                     |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/>                                                           |
| \_DuplexModeValue\_<br/>     | string<br/> | N/D<br/>        | Automático, Manual.<br/>                                                                                                                                                         | Define el modo dúplex. El dúplex automático lo realiza el hardware. El dúplex manual lo realizan el software y el usuario.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>contenido lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




