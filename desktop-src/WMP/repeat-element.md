---
title: ELEMENTO REPEAT
description: El elemento REPEAT define el número de veces Reproductor de Windows Media repite uno o varios elementos ENTRY o ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Elemento REPEAT Reproductor de Windows Media
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476200"
---
# <a name="repeat-element"></a>ELEMENTO REPEAT

El **elemento REPEAT** define el número de veces Reproductor de Windows Media repite uno o varios elementos **ENTRY** **o ENTRYREF.**

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Atributos

**COUNT**

Entero que representa el número de Reproductor de Windows Media repite los elementos **ENTRY** y **ENTRYREF** dentro del ámbito de este elemento.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                |
|-----------------|-------------------------|
| Elementos primarios | **ASX**                 |
| Elementos secundarios  | **ENTRY**, **ENTRYREF** |



 

## <a name="remarks"></a>Observaciones

Este elemento define el número de veces que Reproductor de Windows Media, o recorre en bucle, los clips definidos por los elementos **ENTRY** y **ENTRYREF** dentro del ámbito de este elemento. Solo es válido **el primer elemento REPEAT** de un metarchivo; Se **omiten los elementos REPEAT** posteriores.

Si no se define ningún atributo **COUNT,** el contenido de los elementos **ENTRY** y **ENTRYREF** asociados repite un número infinito de veces. Un valor de cero hace Reproductor de Windows Media omitir el **elemento REPEAT** y reproducir el contenido una vez.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





