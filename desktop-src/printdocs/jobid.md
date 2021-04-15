---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105649331"
---
# <a name="jobid"></a>JobID

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica un identificador único para el trabajo.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [Contenido de lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                     |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Propiedad<br/> |
| Prefijo de ámbito <br/> | Trabajo<br/>      |
| Notas <br/>          | Ninguno<br/>     |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                      | Tipo de datos         | Unidad | Valores admitidos | Resumen |
|---------------------------|-------------------|------|------------------|---------|
| \_JobIDValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Contenido de lenguaje de marcado extensible (XML)

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




