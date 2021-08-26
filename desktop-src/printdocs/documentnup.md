---
description: Obtenga información sobre el elemento DocumentNUp, que describe la salida y el formato de varias páginas lógicas en una sola hoja física.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0804d38bdb60cd28ba88832b21abe8426d8aaf3b4fedf6ce5ad38f624f10c596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949735"
---
# <a name="documentnup"></a>DocumentNUp

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe la salida y el formato de varias páginas lógicas en una sola hoja física. Cada documento se compila por separado. DocumentNUp y JobNUpAllDocumentsContiguously son mutuamente excluyentes. Es el controlador quien determina el control de restricciones entre estas palabras clave.

En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene 2 páginas. Cada documento se dúplex por separado. La dirección de presentación que se muestra a continuación es la opción RightBottom.

![un diagrama que muestra cómo se estableciendo las páginas del documento en una sola hoja en función de la configuración de documentnup](images/local-1663869164-docduplex1.gif)

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [lenguaje de marcado extensible (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Value |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento <br/>   | Característica<br/>                                                                                                                              |
| Prefijo de ámbito <br/> | Documento<br/>                                                                                                                             |
| Notas <br/>          | Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica mediante el origen del eje X y el eje Y.<br/> |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es la siguiente:

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                                           | Tipo de datos          | Unidad                     | Valores admitidos                                                                                                                                                                      | Resumen                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>                      | string<br/>  | caracteres<br/>    | Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | string<br/>  | N/D<br/>           | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | integer<br/> | Páginas lógicas<br/> | Todos los enteros (mayor que cero).<br/>                                                                                                                                          | Especifica el número de páginas lógicas por hoja física. El conjunto admitido puede ser cualquier conjunto de enteros, por ejemplo. {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | string<br/>  | caracteres<br/>    | Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




