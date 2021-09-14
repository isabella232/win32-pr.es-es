---
title: ELEMENTO AUTHOR
description: El elemento AUTHOR contiene el nombre del autor de un metarchivo Windows multimedia o clip multimedia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento AUTHOR Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889857"
---
# <a name="author-element"></a>ELEMENTO AUTHOR

El **elemento AUTHOR** contiene el nombre del autor de un Windows multimedia o clip multimedia.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento            |
|-----------------|--------------------|
| Elementos primarios | **ASX**, **ENTRY** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento contiene una cadena de texto que representa el nombre del autor de un Windows multimedia o clip multimedia. Puede usar el elemento **AUTHOR dentro** del elemento **ASX** y dentro de **los elementos ENTRY.**

Si este elemento aparece en el **elemento ASX,** el texto se muestra como **Mostrar** información.

Si este elemento aparece en un **elemento ENTRY,** el texto se muestra como el autor del clip.

Cada elemento **ASX y** **ENTRY** primario debe contener como máximo un elemento **AUTHOR** secundario. Varios **elementos AUTHOR** después de la primera se omitirán y no se mostrarán.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





