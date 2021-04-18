---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b022d9c8067f330e14697932382c4c8f058a8f3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105721401"
---
# <a name="documentcollate"></a>DocumentCollate

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe las características de intercalación de la salida. Se intercalan todas las páginas de cada documento individual. DocumentCollate y JobCollateAlldocuments se excluyen mutuamente. El comportamiento y la implementación de si se ha implementado o solo una de estas palabras clave se deja al controlador.

A continuación se indican las reglas que deben seguirse para la implementación de intercalación

## <a name="element-definition-and-rules"></a>Definición de elementos y reglas

En primer lugar, debe seguir las reglas de JobCollateAllDocument y, a continuación, aplicar las reglas de DocumentCollate para que los escenarios funcionen. Tenga en cuenta que en la configuración de la conversión de PrintTicket a DEVMODE, donde JobCollateAllDocuments no es compatible con el controlador, depende del controlador elegir el comportamiento adecuado que se debe llevar a cabo (JobCollateAllDocuments = ON u OFF). Además, la opción se puede cambiar en función de otras opciones de PrintTicket.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

EN: copias de impresión (DocumentCopiesAllPages) de cada documento, repita JobCopiesAllDocuments veces.

Desactivado: para cada documento, imprime (JobCopiesAllDocuments x DocumentCopiesAllPages) copias juntas.

### <a name="documentcollate"></a>DocumentCollate

ACTIVADO: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de un documento que se imprime de forma contigua, intercalar hojas en dicho documento.

OFF: para todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) impresas de forma contigua, imprime todas las copias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada hoja juntas.

-   [Información de elemento](#element-information)

-   [Contenido estructural](#structural-content)

-   [Contenido XML](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                     |
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
| \_OptionName\_<br/>          | string<br/> | caracteres<br/> | Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenido de lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres. El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

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

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




