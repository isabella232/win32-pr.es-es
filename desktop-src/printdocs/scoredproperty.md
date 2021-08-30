---
description: Busque información sobre el elemento ScoredProperty. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ad42d49e65fffebad0aec7730ab8ce85f41876
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882229"
---
# <a name="scoredproperty"></a>ScoredProperty

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ScoredProperty declara una propiedad intrínseca a una definición de opción. Estas propiedades se deben comparar al evaluar el nivel de coincidencia de una opción solicitada con una opción compatible con el dispositivo.

## <a name="element-tag"></a>Etiqueta de elemento

&lt;ScoredProperty&gt;

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo name de ScoredProperty, ya sea una propiedad estándar o una propiedad definida de forma privada. <br/> |



 

Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | *Opción*<br/> *ScoredProperty*<br/>                                                                                                                          |
| Elementos secundarios<br/>  | Es posible usar el<br/> *ParameterRef* (uno)<br/> o<br/> *Valor* (uno)<br/> *Propiedad* (cero o más)<br/> *ScoredProperty* (cero o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados del mismo nivel.<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que un elemento ScoredProperty no tenga dependencias de configuración.

## <a name="example"></a>Ejemplo

Declare un elemento ScoredProperty denominado MediaSizeWidth con un valor de 11.

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




