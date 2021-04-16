---
title: Elemento REPEAT
description: El elemento REPEAT define el número de veces que Windows Media Player repetirá uno o varios elementos ENTRYREF o ENTRY.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Ventanas de elementos de repetición Media Player
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650049"
---
# <a name="repeat-element"></a>Elemento REPEAT

El elemento **REPEAT** define el número de veces que Windows Media Player repetirá uno o varios elementos **ENTRYREF** o **entry** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Atributos

**COUNT**

Entero que representa el número de veces que Windows Media Player repite los elementos **entry** y **ENTRYREF** dentro del ámbito de este elemento.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                |
|-----------------|-------------------------|
| Elementos primarios | **ASX**                 |
| Elementos secundarios  | **entry**, **ENTRYREF** |



 

## <a name="remarks"></a>Observaciones

Este elemento define el número de veces que Windows Media Player repite, o recorre en bucle, los clips definidos por los elementos **entry** y **ENTRYREF** dentro del ámbito de este elemento. Solo es válido el primer elemento **REPEAT** de un metarchivo; los elementos de **repetición** subsiguientes se omiten.

Si no se define ningún atributo de **recuento** , el contenido de los elementos de **entrada** y **ENTRYREF** asociados se repite un número infinito de veces. Un valor de cero hace que Windows Media Player omita el elemento **REPEAT** y reproduzca el contenido una vez.

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





