---
description: Obtenga información sobre el elemento DocumentCollate, que describe las características de intercalación de la salida.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409458"
---
# <a name="documentcollate"></a>DocumentCollate

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe las características de intercalación de la salida. Se intercalan todas las páginas de cada documento individual. DocumentCollate y JobCollateAlldocuments son mutuamente excluyentes. El comportamiento y la implementación de si se implementan ambas o solo una de estas palabras clave se deja al controlador.

A continuación se deberán seguir las reglas para la implementación de Collate.

## <a name="element-definition-and-rules"></a>Definición y reglas de elementos

Primero debe seguir las reglas de JobCollateAllDocument y, a continuación, aplicar las reglas de DocumentCollate para que los escenarios funcionen. Tenga en cuenta que en un valor de conversión PrintTicket a Devmode, donde JobCollateAllDocuments no es compatible con el controlador, es el controlador el que elige el comportamiento adecuado que se debe tomar (JobCollateAllDocuments = ON u OFF). Además, la opción se puede cambiar en función de otras opciones de PrintTicket.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

ON: imprima (DocumentCopiesAllPages) copias de cada documento, repita JobCopiesAllDocuments veces.

OFF: para cada documento, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntos.

### <a name="documentcollate"></a>DocumentCollate

ON: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de un documento impreso de forma contigua, intercala las hojas de ese documento.

OFF: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) impresas de forma contigua, imprima todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada hoja juntas.

-   [Información de elemento](#element-information)

-   [Contenido estructural](#structural-content)

-   [Contenido XML](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Característica<br/>  |
| Prefijo de ámbito <br/> | Documento<br/> |
| Notas <br/>          | Ninguno<br/>     |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:DocumentCollate">
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
| \_OptionName\_<br/>          | string<br/> | caracteres<br/> | Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




