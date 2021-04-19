---
title: Elemento AUTHOR
description: El elemento AUTHOR contiene el nombre del autor de un metarchivo de Windows Media o de un clip multimedia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento de autor de Windows Media Player
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698732"
---
# <a name="author-element"></a>Elemento AUTHOR

El elemento **Author** contiene el nombre del autor de un metarchivo de Windows Media o de un clip multimedia.

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
| Elementos primarios | **ASX**, **entrada** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento contiene una cadena de texto que representa el nombre del autor de un metarchivo de Windows Media o un clip multimedia. Puede usar el elemento **Author** dentro del elemento **ASX** y dentro de los elementos de **entrada** .

Si este elemento aparece en el elemento **ASX** , el texto se muestra como **Mostrar** información.

Si este elemento aparece en un elemento de **entrada** , el texto se muestra como autor del clip.

Cada elemento **ASX** y **entry** primarios debe contener como máximo un elemento secundario **Author** . Varios elementos **Author** después del primero se omitirán y no se mostrarán.

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





