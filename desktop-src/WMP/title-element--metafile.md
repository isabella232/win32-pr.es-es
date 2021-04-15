---
title: TITLE (elemento) (metarchivo)
description: El elemento TITLE define una cadena de texto que especifica el título de un elemento ASX o ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (metarchivo) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709082"
---
# <a name="title-element-metafile"></a>TITLE (elemento) (metarchivo)

El elemento **title** define una cadena de texto que especifica el título de un elemento **ASX** o **entry** .

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
| Elementos primarios | **ASX**, **entrada** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define una cadena de texto que especifica el título de un elemento **ASX** o **entry** . El título se muestra en el panel de información y en el cuadro de diálogo **propiedades** .

Cuando este elemento aparece dentro de un elemento **ASX** , el texto se muestra como **Mostrar** información. Cuando este elemento aparece dentro de un elemento de **entrada** , el texto se muestra como información de **recorte** .

Si un elemento **MOREINFO** también se usa con el elemento (primario) asociado, es el texto del título en el que el usuario hace clic para obtener acceso a la dirección URL definida en el elemento **MOREINFO** .

Cada elemento **ASX** y **entry** primarios debe contener como máximo un elemento secundario **title** . Varios elementos **title** después del primero se omitirán y no se mostrarán.

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





