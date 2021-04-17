---
title: Elemento STARTMARKER
description: El elemento STARTMARKER especifica un marcador desde el que Windows Media Player comenzará a representar la secuencia.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Elemento STARTMARKER Media Player Windows
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700116"
---
# <a name="startmarker-element"></a>Elemento STARTMARKER

El elemento **STARTMARKER** especifica un marcador desde el que Windows Media Player comenzará a representar la secuencia.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Atributos

**NÚMEROS**

El número de un marcador numérico en el índice. El valor predeterminado es el principio del contenido a petición o la posición actual en un flujo en tiempo real.

**NOMBRE**

Nombre de un marcador con nombre en el índice. El valor predeterminado es el principio del contenido a petición o la posición actual en un flujo en tiempo real.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **entrada**, **ref** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento especifica el marcador desde el que Windows Media Player va a comenzar a representar la secuencia definida en el elemento primario **entry** o **ref** .

**Note**

Use este elemento con el atributo **número** o **nombre** , pero no ambos.

Un elemento **STARTMARKER** definido dentro de un elemento **ref** tiene prioridad sobre un elemento **STARTMARKER** definido en el elemento de **entrada** primario del elemento **ref** . Un elemento **STARTMARKER** también tiene prioridad sobre un elemento **STARTTIME** .

Si el marcador especificado por un elemento **STARTMARKER** se produce posteriormente en la secuencia que el marcador definido por un elemento **ENDMARKER** , no se reproduce ningún contenido, pero no se genera ningún error.

## <a name="examples"></a>Ejemplos


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





