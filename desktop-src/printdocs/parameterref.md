---
description: Obtenga información sobre el elemento ParameterRef, que define una referencia a un elemento ParameterInit y cómo funciona con ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407188"
---
# <a name="parameterref"></a>ParameterRef

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterRef define una referencia a un elemento ParameterInit. Un elemento ScoredProperty que contiene un elemento ParameterRef no tiene un elemento Value establecido explícitamente. En su lugar, el elemento ScoredProperty recibe su valor del elemento ParameterInit al que hace referencia un elemento ParameterRef.

## <a name="element-tag"></a>Etiqueta de elemento

<ParameterRef>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo name del elemento ParameterDef al que se hace referencia en el contexto del documento actual.<br/> |



 

Para más información, consulte la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | ScoredProperty <br/>                                                                        |
| Elementos secundarios<br/>  | No se permite ninguna.<br/>                                                                        |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados relacionados.<br/> |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que los elementos ParameterRef no tengan dependencias de configuración.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar elementos ParameterRef para permitir que los usuarios escriban parámetros de tamaño multimedia personalizados.

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

 

 




