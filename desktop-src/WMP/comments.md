---
title: Comentarios (msfeeds. h)
description: Agregue comentarios a los metaarchivos siguiendo la sintaxis de lenguaje de marcado extensible (XML). Los comentarios comienzan con \ 0034; --\ 0034; y terminan con \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Comentarios Media Player de Windows
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
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700415"
---
# <a name="comments-msfeedsh"></a>Comentarios (msfeeds. h)

Agregue comentarios a los metaarchivos siguiendo la sintaxis de lenguaje de marcado extensible (XML). Los comentarios comienzan con " &lt; !--" y terminan con "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Observaciones

Los comentarios pueden aparecer en cualquier lugar excepto en el contenido del elemento (entre las etiquetas de apertura y cierre de elemento,  < >). No forman parte de los datos de caracteres del documento y se omiten cuando se analiza el metarchivo.

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
| Encabezado<br/> | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





