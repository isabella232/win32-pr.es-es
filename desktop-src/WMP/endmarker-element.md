---
title: Elemento ENDMARKER
description: El elemento ENDMARKER especifica un marcador en el que Windows Media Player detendrá la representación de la secuencia.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Elemento ENDMARKER Media Player Windows
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700324"
---
# <a name="endmarker-element"></a>Elemento ENDMARKER

El elemento **ENDMARKER** especifica un marcador en el que Windows Media Player detendrá la representación de la secuencia.

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Atributos

**NÚMEROS**

El número de un marcador numérico en el índice. El valor predeterminado es el final del contenido.

**NOMBRE**

Nombre de un marcador con nombre en el índice. El valor predeterminado es el final del contenido.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **entrada**, **ref** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica el marcador donde Windows Media Player va a detener la representación de la secuencia definida en el elemento primario **entry** o **ref** .

Nota

Use el elemento **ENDMARKER** con el atributo **número** o **nombre** , pero no ambos.

En el modo de vista previa, al alcanzar un marcador final se detiene la vista previa, incluso si no ha transcurrido el tiempo especificado por el elemento **PREVIEWDURATION** . El elemento **ENDMARKER** también tiene prioridad sobre el elemento **Duration** .

Un elemento **ENDMARKER** definido dentro de un elemento **ref** tiene prioridad sobre un **ENDMARKER** definido en el elemento de **entrada** primario del elemento **ref** .

Si el marcador especificado por un elemento **ENDMARKER** se produce antes en el flujo que el marcador definido por un elemento **STARTMARKER** , no se reproduce ningún contenido, pero no se genera ningún error.

## <a name="examples"></a>Ejemplos


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





