---
description: Obtenga información sobre el elemento JobNUpAllDocumentsContiguously, que describe la salida de varias páginas lógicas en una sola hoja física.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360678"
---
# <a name="jobnupalldocumentscontiguously"></a>JobNUpAllDocumentsContiguously

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe la salida de varias páginas lógicas en una sola hoja física. Todos los documentos del trabajo se compilan juntos de forma contigua. JobNUpAllDocumentsContiguously y DocumentNUp son mutuamente excluyentes. Es el controlador quien determina el control de restricciones entre estas palabras clave.

En el diagrama siguiente se muestra un ejemplo con el documento 1 que contiene 3 páginas y el documento 2 que contiene 2 páginas. Cada documento del trabajo se dúplex de forma contigua. Las direcciones de presentación que se muestran en el ejemplo son la opción RightBottom.

![diagrama que muestra cómo se estableciendo las páginas del documento en una sola hoja en función de la configuración de documentnup](images/local-1242234459-jobduplexpics.gif)

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [lenguaje de marcado extensible (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Value |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento <br/>   | Característica<br/>                                                                                                                             |
| Prefijo de ámbito <br/> | Trabajo<br/>                                                                                                                                 |
| Notas <br/>          | Top, Bottom, Left y Right son relativos a PageImageableSize, donde TopLeft se indica por el origen del alto y el ancho.<br/> |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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
| \_OptionName\_<br/>                      | string<br/>  | caracteres<br/>    | Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | string<br/>  | N/D<br/>           | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | integer<br/> | Páginas lógicas<br/> | Todos los enteros (mayor que cero).<br/>                                                                                                                                          | Especifica el número de páginas lógicas por hoja física. El conjunto admitido puede ser cualquier conjunto de enteros, por ejemplo. {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | string<br/>  | caracteres<br/>    | Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




