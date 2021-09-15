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
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465845"
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

Este elemento define una cadena de texto que especifica el título de un **elemento ASX** o **ENTRY.** El título se muestra en el panel de pantalla y en el **cuadro de diálogo** Propiedades.

Cuando este elemento aparece dentro de un **elemento ASX,** el texto se muestra como **Mostrar** información. Cuando este elemento aparece dentro de **un elemento ENTRY,** el texto se muestra como **Información de** recorte.

Si también se usa un elemento **MOREINFO** con el elemento asociado (primario), es el texto del título en el que el usuario hace clic para acceder a la dirección URL definida en el **elemento MOREINFO.**

Cada elemento **PRIMARIO ASX** y **ENTRY** debe contener como máximo un elemento **SECUNDARIO TITLE.** Se **omitirán** varios elementos TITLE después del primero y no se mostrarán.

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

 

 





