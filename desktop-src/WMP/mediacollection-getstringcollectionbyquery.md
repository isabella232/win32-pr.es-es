---
title: MediaCollection. getStringCollectionByQuery, método
description: El método getStringCollectionByQuery recupera un objeto StringCollection que contiene todas las cadenas que coinciden con las condiciones de la consulta.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- método getStringCollectionByQuery de Windows Media Player
- método getStringCollectionByQuery de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getStringCollectionByQuery
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
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690296"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>MediaCollection. getStringCollectionByQuery, método

El método **getStringCollectionByQuery** recupera un objeto **StringCollection** que contiene todas las cadenas que coinciden con las condiciones de la consulta.

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

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*consulta* \[ de de\]
</dt> <dd>

Objeto de **consulta** .

</dd> <dt>

*mediaType* \[ de\]
</dt> <dd>

**Cadena** que contiene el tipo de medio. Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".

</dd> <dt>

*sortAttribute* \[ de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo utilizado para la ordenación. Una cadena vacía ("") significa que no se aplica ninguna ordenación.

</dd> <dt>

*sortAscending* \[ de\]
</dt> <dd>

**Boolean**, true, que indica que el objeto **StringCollection** debe estar ordenado en orden ascendente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **StringCollection** .

## <a name="remarks"></a>Observaciones

Las consultas compuestas que usan la **consulta** no distinguen mayúsculas de minúsculas.

Cuando la consulta compuesta especificada por el parámetro de *consulta* contiene una condición generada en el atributo **mediatype** , se omite esa condición. Siempre se usa el valor del parámetro *mediaType* . Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *mediatype* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaType (atributo)**](mediatype-attribute.md)
</dt> <dt>

[**Query (objeto)**](query-object.md)
</dt> </dl>

 

 





