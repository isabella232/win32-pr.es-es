---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717421"
---
# <a name="parameterref"></a>ParameterRef

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterRef define una referencia a un elemento ParameterInit. Un elemento ScoredProperty que contiene un elemento ParameterRef no tiene un elemento de valor establecido explícitamente. En su lugar, el elemento ScoredProperty recibe su valor del elemento ParameterInit al que hace referencia un elemento ParameterRef.

## <a name="element-tag"></a>Etiqueta de elemento

<ParameterRef>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo name del elemento ParameterDef al que se hace referencia en el contexto del documento actual.<br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | ScoredProperty <br/>                                                                        |
| Elementos secundarios<br/>  | Ninguno permitido.<br/>                                                                        |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten nodos secundarios duplicados.<br/> |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Los elementos ParameterRef no pueden tener dependencias de configuración.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar los elementos ParameterRef para permitir que los usuarios escriban parámetros de tamaño multimedia personalizados.

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




