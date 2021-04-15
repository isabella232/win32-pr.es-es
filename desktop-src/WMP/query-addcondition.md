---
title: Query. addCondition (método)
description: El método addCondition agrega una condición al objeto de consulta mediante la lógica y.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- método addCondition de Windows Media Player
- método addCondition de Windows Media Player, clase de consulta
- Clase de consulta de Windows Media Player, método addCondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708278"
---
# <a name="queryaddcondition-method"></a>Query. addCondition (método)

El método **addCondition** agrega una condición al objeto de **consulta** mediante la lógica y.

## <a name="syntax"></a>Sintaxis


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*operador* \[ de de\]
</dt> <dd>

**Cadena** que contiene el operador. Vea la sección Comentarios para ver los valores admitidos.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

**Cadena** que contiene el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las consultas compuestas que usan la **consulta** no distinguen mayúsculas de minúsculas.

Puede encontrar una lista de valores para el parámetro de *atributo* en la sección de [referencia de atributo alfabético](alphabetical-attribute-reference.md) .

Las condiciones contenidas en un objeto de **consulta** se organizan en grupos de condiciones. Varias condiciones dentro de un grupo de condiciones se concatenan siempre mediante la lógica y. Los grupos de condiciones siempre se concatenan entre sí mediante la lógica o. Para iniciar un nuevo grupo de condiciones, llame a **query. beginNextGroup**.

En la tabla siguiente se enumeran los valores admitidos para el *operador*.



| Operator            | Se aplica a     |
|---------------------|----------------|
| BeginsWith          | Cadenas        |
| Contiene            | Cadenas        |
| Equals              | Todos los tipos      |
| GreaterThan         | Números, fechas |
| GreaterThanOrEquals | Números, fechas |
| LessThan            | Números, fechas |
| LessThanOrEquals    | Números, fechas |
| NotBeginsWith       | Cadenas        |
| NotContains         | Cadenas        |
| NotEquals           | Todos los tipos      |



 

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa **query. addCondition** y **query. beginNextGroup** para realizar una consulta de ejemplo.


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Query (objeto)**](query-object.md)
</dt> <dt>

[**Consulta. beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





