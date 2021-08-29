---
title: Elemento ENDMARKER
description: El elemento ENDMARKER especifica un marcador en el que Reproductor de Windows Media dejará de representar la secuencia.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Elemento ENDMARKER Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 276b17117d2f01d9bc40d7f171a6d0ff6ea2331da439266ac11bf8c25b5e4f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996670"
---
# <a name="endmarker-element"></a>Elemento ENDMARKER

El **elemento ENDMARKER** especifica un marcador en el que Reproductor de Windows Media dejará de representar la secuencia.

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Atributos

**Número**

Número de un marcador numérico en el índice. El valor predeterminado es el final del contenido.

**NOMBRE**

Nombre de un marcador con nombre en el índice. El valor predeterminado es el final del contenido.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ENTRY**, **REF** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica el marcador en el Reproductor de Windows Media para detener la representación de la secuencia definida en el elemento **primario ENTRY** o **REF.**

Nota

Use el **elemento ENDMARKER** con el atributo **NUMBER** o **NAME,** pero no ambos.

En el modo de vista previa, al llegar a un marcador final se detiene la vista previa, incluso si no ha transcurrido el tiempo especificado por el **elemento PREVIEWDURATION.** El **elemento ENDMARKER** también tiene prioridad sobre el **elemento DURATION.**

Un **elemento ENDMARKER** definido dentro de un elemento **REF** tiene  prioridad sobre **un ENDMARKER** definido dentro del elemento PRIMARIO ENTRY del **elemento REF.**

Si el marcador especificado por un elemento **ENDMARKER** se produce antes en la secuencia que el marcador definido por un **elemento STARTMARKER,** no se reproduce contenido, pero no se genera ningún error.

## <a name="examples"></a>Ejemplos


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





