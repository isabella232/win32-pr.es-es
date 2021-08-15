---
title: elemento media
description: El elemento multimedia especifica uno de los elementos multimedia de una lista de reproducción.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- elemento media Reproductor de Windows Media
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c67f4321d85ec52babbc6f24c2cd9e3512f7c970eb3360ba2ddfd7ba53f82152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996325"
---
# <a name="media-element"></a>elemento media

El **elemento multimedia** especifica uno de los elementos multimedia de una lista de reproducción.

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
| <span id="cid"></span><span id="CID"></span>**Cid**<br/>                                                             | Identificador de contenido que es único para este elemento multimedia.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**Tid**<br/>                                                             | Identificador de seguimiento que se puede usar para realizar el seguimiento del objeto del sistema de archivos para este elemento multimedia.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos               |
|-----------|------------------------|
| Parent    | [Seq](seq-element.md) |
| Elemento secundario     | Ninguno                   |



 

## <a name="remarks"></a>Observaciones

El **atributo cid** (el identificador de contenido) se rellena mediante el Reproductor de Windows Media como una manera de identificar de forma única un fragmento de contenido multimedia incluso si se han cambiado sus atributos de metadatos. Esto permite el uso compartido de listas de reproducción entre equipos, ya que el contenido se puede identificar en otro equipo y la ruta de acceso a él puede ser "reparada automáticamente" por la lista de reproducción multimedia de Windows. El **atributo tid** (el identificador de seguimiento) usa el sistema de archivos Windows para reparar automáticamente la ruta de acceso al medio si se cambia el nombre o la ubicación del archivo.

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



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**seq (Elemento)**](seq-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





