---
title: Método MediaCollection.getPlaylistByQuery
description: El método getPlaylistByQuery recupera un objeto Playlist que contiene objetos Media que coinciden con las condiciones de consulta.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- Método getPlaylistByQuery Reproductor de Windows Media
- Método getPlaylistByQuery Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f64f054fe59865fb8d213d343696c86d83a5f8698d498c854660f76dc9085f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837148"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Método MediaCollection.getPlaylistByQuery

El **método getPlaylistByQuery** recupera un objeto **Playlist** que contiene objetos **Media** que coinciden con las condiciones de consulta.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*consulta* \[ En\]
</dt> <dd>

**Objeto** de consulta que define las condiciones usadas para crear la lista de reproducción.

</dd> <dt>

*mediaType* \[ En\]
</dt> <dd>

**Cadena** que contiene el tipo de medio. Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".

</dd> <dt>

*sortAttribute* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre de atributo utilizado para la ordenación. Una cadena vacía ("") significa que no se aplica ninguna ordenación.

</dd> <dt>

*sortAscending* \[ En\]
</dt> <dd>

**Booleano**, true que indica que la lista de reproducción debe ordenarse en orden ascendente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Comentarios

Las consultas compuestas **que usan consulta** no distinguen mayúsculas de minúsculas.

Cuando la consulta compuesta especificada por el parámetro *de* consulta contiene una condición creada en el **atributo MediaType,** esa condición se omite. Siempre se usa el valor del parámetro *mediaType.* Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *mediaType* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Atributo MediaType**](mediatype-attribute.md)
</dt> <dt>

[**Objeto Query**](query-object.md)
</dt> </dl>

 

 





