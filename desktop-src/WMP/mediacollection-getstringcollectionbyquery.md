---
title: Método MediaCollection.getStringCollectionByQuery
description: El método getStringCollectionByQuery recupera un objeto StringCollection que contiene todas las cadenas que coinciden con las condiciones de consulta.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Método getStringCollectionByQuery Reproductor de Windows Media
- Método getStringCollectionByQuery Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e8f2eae2ce52a566d4db6b8298187df1d4d444432e99dda22d3cacc0ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390116"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>Método MediaCollection.getStringCollectionByQuery

El **método getStringCollectionByQuery** recupera un **objeto StringCollection** que contiene todas las cadenas que coinciden con las condiciones de consulta.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*consulta* \[ En\]
</dt> <dd>

**Objeto de** consulta.

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

**Booleano**, true que indica que **StringCollection** debe ordenarse en orden ascendente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto StringCollection.**

## <a name="remarks"></a>Comentarios

Las consultas compuestas que **usan consulta** no distinguen mayúsculas de minúsculas.

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

 

 





