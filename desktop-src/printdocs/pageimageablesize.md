---
description: Obtenga información sobre el elemento configurable por el usuario PageImageableSize. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 924c89f304c75863246f266e2c64818ee7ab21c173009a096d32c3d1ac6e178b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948275"
---
# <a name="pageimageablesize"></a>PageImageableSize

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe el lienzo con imágenes para el diseño y la representación. Esto se mostrará en función de PageMediaSize y PageOrientation.

En los diagramas siguientes se muestra el uso de variables PageImageableSize basadas en PageOrientation.

![un diagrama que muestra las medidas de página](images/local-1641910626-image.png)

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [contenido lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento

| Nombre                 | Value         |
|----------------------|---------------|
| Tipo de elemento<br/>    | Propiedad<br/> |
| Prefijo de ámbito <br/> | Página<br/>     |
| Notas <br/>          | Ninguno<br/>     |

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                                    | Tipo de datos          | Unidad               | Valores admitidos                       | Resumen                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_ImageableSizeWidthValue\_<br/>  | integer<br/> | Micras<br/> | Mayor que 0.<br/>             | Especifica la dimensión horizontal del tamaño del medio de aplicación con respecto a PageOrientation.<br/>               |
| \_ImageableSizeHeightValue\_<br/> | integer<br/> | Micras<br/> | Mayor que 0.<br/>             | Especifica la dimensión vertical del tamaño del medio de la aplicación con respecto a PageOrientation.<br/>                 |
| \_OriginWidthValue\_<br/>         | integer<br/> | Micras<br/> | Mayor o igual que 0.<br/> | Especifica el origen horizontal del área en la que se pueden crear imágenes en relación con el tamaño del medio de la aplicación.<br/>                   |
| \_OriginHeightValue\_<br/>        | integer<br/> | Micras<br/> | Mayor o igual que 0.<br/> | Especifica el origen vertical del área en la que se pueden crear imágenes en relación con el tamaño del medio de la aplicación.<br/>                     |
| \_ExtentWidthValue\_<br/>         | integer<br/> | Micras<br/> | Mayor que 0.<br/>             | Especifica la distancia horizontal entre el origen y el límite del tamaño del medio de la aplicación.<br/>      |
| \_ExtentHeightValue\_<br/>        | integer<br/> | Micras<br/> | Mayor que 0.<br/>             | Especifica la distancia vertical entre el origen y el límite del tamaño del medio de la aplicación de lienzo.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>contenido lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




