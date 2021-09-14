---
title: Método Query.addCondition
description: El método addCondition agrega una condición al objeto Query mediante la lógica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Método addCondition Reproductor de Windows Media
- método addCondition Reproductor de Windows Media , clase Query
- Clase de consulta Reproductor de Windows Media , método addCondition
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073229"
---
# <a name="queryaddcondition-method"></a>Método Query.addCondition

El **método addCondition** agrega una condición al **objeto Query** mediante la lógica AND.

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

*atributo* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo.

</dd> <dt>

*operador* \[ En\]
</dt> <dd>

**Cadena** que contiene el operador . Consulte Comentarios para ver los valores admitidos.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

**Cadena** que contiene el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las consultas compuestas que **usan Query** no distinguen mayúsculas de minúsculas.

Puede encontrar una lista de valores para el *parámetro de* atributo en la sección Referencia alfabética [de atributos.](alphabetical-attribute-reference.md)

Las condiciones contenidas en un **objeto Query** se organizan en grupos de condiciones. Varias condiciones dentro de un grupo de condiciones siempre se concatenan mediante la lógica AND. Los grupos de condiciones siempre se concatenan entre sí mediante la lógica OR. Para iniciar un nuevo grupo de condiciones, llame **a Query.beginNextGroup**.

En la tabla siguiente se enumeran los valores admitidos para el *operador*.



| Operator            | Se aplica a     |
|---------------------|----------------|
| BeginsWith          | Cadenas        |
| Contiene            | Cadenas        |
| es igual a              | Todos los tipos      |
| GreaterThan         | Números, fechas |
| GreaterThanOrEquals | Números, fechas |
| LessThan            | Números, fechas |
| LessThanOrEquals    | Números, fechas |
| NotBeginsWith       | Cadenas        |
| NotContains         | Cadenas        |
| NotEquals           | Todos los tipos      |



 

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se **usa Query.addCondition** y **Query.beginNextGroup** para realizar una consulta de ejemplo.


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
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Objeto Query**](query-object.md)
</dt> <dt>

[**Query.beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





