---
title: Comentarios (Msfeeds.h)
description: Agregue comentarios a metarchivos siguiendo la sintaxis lenguaje de marcado extensible (XML). Los comentarios comienzan por \ 0034; -- \ 0034; y terminan con \ 0034;-- \ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Comentarios Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fe5aaf9dde3d804bb91a1e2551636c86aa54ff2bec599bf06100ee2622b592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135788"
---
# <a name="comments-msfeedsh"></a>Comentarios (Msfeeds.h)

Agregue comentarios a metarchivos siguiendo la sintaxis lenguaje de marcado extensible (XML). Los comentarios comienzan &lt; por "!--" y terminan con &gt; "--".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Comentarios

Los comentarios pueden aparecer en cualquier lugar excepto dentro del contenido del elemento (entre etiquetas de apertura y cierre de elementos,  < >). No forman parte de los datos de caracteres del documento y se omiten cuando se analiza el metarchivo.

## <a name="examples"></a>Ejemplos


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





