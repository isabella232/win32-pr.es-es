---
description: Obtenga información sobre cómo el elemento JobCollateAllDocuments describe las características de intercalación de la salida. Todos los documentos de cada trabajo individual se intercalan.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5e9adc0b6e9682f3c67f1bc8f5ef46c5e272c434968c3c1490e474b7edc0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971314"
---
# <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe las características de intercalación de la salida. Todos los documentos de cada trabajo individual se intercalan. DocumentCollate y JobCollateAlldocuments son mutuamente excluyentes. El comportamiento y la implementación de si se implementan ambas o solo una de estas palabras clave se deja al controlador.

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
-   [contenido lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

### <a name="element-information"></a>Información de elemento



| Nombre | Value |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Característica<br/> |
| Prefijo de ámbito <br/> | Trabajo<br/>     |
| Notas <br/>          | Ninguno<br/>    |



 

### <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                               | Tipo de datos         | Unidad                  | Valores admitidos                                                                                                                                                                      | Resumen                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caracteres<br/> | Nombre completo válido tal y como se define en [Espacios de nombres en XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |



 

### <a name="extensible-markup-language-xml-content"></a>contenido lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




