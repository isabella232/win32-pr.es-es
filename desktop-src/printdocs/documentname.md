---
description: Obtenga información sobre la propiedad DocumentName, que especifica un nombre descriptivo para el documento.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: DocumentName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e5cee22cbfe462b66fb7291156e1a325b17758ae402d201a847470297f8e11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092105"
---
# <a name="documentname"></a>DocumentName

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica un nombre descriptivo para el documento.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [lenguaje de marcado extensible (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Propiedad<br/> |
| Prefijo de ámbito <br/> | Documento<br/> |
| Notas <br/>          | Ninguno<br/>     |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es la siguiente:

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                             | Tipo de datos         | Unidad | Valores admitidos | Resumen |
|----------------------------------|-------------------|------|------------------|---------|
| \_DocumentNameValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




