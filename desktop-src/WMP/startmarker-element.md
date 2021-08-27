---
title: Elemento STARTMARKER
description: El elemento STARTMARKER especifica un marcador desde el que Reproductor de Windows Media comenzará a representar la secuencia.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Elemento STARTMARKER Reproductor de Windows Media
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fa80da249edc4b9e3ab7d8796bc6ff135cb7cfb2b19a1cb11216ebe4a9c122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123045"
---
# <a name="startmarker-element"></a>Elemento STARTMARKER

El **elemento STARTMARKER** especifica un marcador a partir del Reproductor de Windows Media comenzará a representar la secuencia.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Atributos

**Número**

Número de un marcador numérico en el índice. El valor predeterminado es el principio del contenido a petición o la posición actual en una secuencia en tiempo real.

**NOMBRE**

Nombre de un marcador con nombre en el índice. El valor predeterminado es el principio del contenido a petición o la posición actual en una secuencia en tiempo real.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ENTRY**, **REF** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica el marcador desde el que Reproductor de Windows Media va a empezar a representar la secuencia definida en el elemento **primario ENTRY** o **REF.**

**Nota**

Use este elemento con el atributo **NUMBER** **o NAME,** pero no con ambos.

Un **elemento STARTMARKER** definido dentro de un **elemento REF** tiene prioridad  sobre un **elemento STARTMARKER** definido dentro del elemento PRIMARIO ENTRY del **elemento REF.** Un **elemento STARTMARKER** también tiene prioridad sobre **un elemento STARTTIME.**

Si el marcador especificado por un elemento **STARTMARKER** se produce más adelante en la secuencia que el marcador definido por un elemento **ENDMARKER,** no se reproduce contenido, pero no se genera ningún error.

## <a name="examples"></a>Ejemplos


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





