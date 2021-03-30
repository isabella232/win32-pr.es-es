---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9fbbfc17582042c6f4f5b5d96838ba48f46825
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "103820450"
---
# <a name="pagetruetypefontmode"></a>PageTrueTypeFontMode

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe el método de control de fuentes TrueType que se va a utilizar.

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
<psf:Feature name="psk:PageTrueTypeFontMode">
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
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




