---
title: ELEMENTO TITLE (metarchivo)
description: El elemento TITLE define una cadena de texto que especifica el título de un elemento ASX o ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (metarchivo) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 085bec9a9937c8dbd02fad6df785f4bce7afea90a74117e745f09cb5135633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117725"
---
# <a name="title-element-metafile"></a>ELEMENTO TITLE (metarchivo)

El **elemento TITLE** define una cadena de texto que especifica el título de un elemento **ASX** **o ENTRY.**

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **ENTRY** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define una cadena de texto que especifica el título de un **elemento ASX** o **ENTRY.** El título se muestra en el panel de presentación y en el **cuadro de diálogo** Propiedades.

Cuando este elemento aparece dentro de un **elemento ASX,** el texto se muestra como **Mostrar** información. Cuando este elemento aparece dentro de un **elemento ENTRY,** el texto se muestra como **Información de** clip.

Si también se usa un elemento **MOREINFO** con el elemento asociado (primario), es el texto del título en el que el usuario hace clic para acceder a la dirección URL definida en el **elemento MOREINFO.**

Cada elemento **ASX y** **ENTRY** primario debe contener como máximo un elemento **SECUNDARIO TITLE.** Varios **elementos TITLE** después de la primera se omitirán y no se mostrarán.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
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

 

 





