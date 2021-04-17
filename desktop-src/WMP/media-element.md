---
title: Elemento multimedia
description: El elemento multimedia especifica uno de los elementos multimedia de una lista de reproducción.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento multimedia Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653301"
---
# <a name="media-element"></a>Elemento multimedia

El elemento **multimedia** especifica uno de los elementos multimedia de una lista de reproducción.

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                       | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obligatorio) <br/> | Dirección URL de un elemento multimedia.<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**Cid**<br/>                                                             | IDENTIFICADOR de contenido que es único para este elemento multimedia.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**TID**<br/>                                                             | El identificador de seguimiento que se puede usar para realizar el seguimiento del objeto del sistema de archivos para este elemento multimedia.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos               |
|-----------|------------------------|
| Parent    | [Próx](seq-element.md) |
| Elemento secundario     | None                   |



 

## <a name="remarks"></a>Observaciones

El atributo **CID** (el ID. de contenido) lo rellena la Media Player de Windows como una manera de identificar de forma única un elemento de contenido multimedia aunque se hayan cambiado sus atributos de metadatos. Esto permite el uso compartido de listas de reproducción en todos los equipos, ya que el contenido se puede identificar en otro equipo, y la ruta de acceso a ella puede ser "reparada automáticamente" por la lista de reproducción de Windows Media. El atributo **TID** (el ID. de seguimiento) usa el sistema de archivos de Windows para reparar automáticamente la ruta de acceso al medio si se cambia el nombre o la ubicación del archivo.

## <a name="examples"></a>Ejemplos


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Seq (elemento)**](seq-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





