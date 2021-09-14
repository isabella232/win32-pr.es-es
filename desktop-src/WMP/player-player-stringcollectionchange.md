---
title: Evento Player.StringCollectionChange
description: El evento StringCollectionChange tiene lugar cuando cambia una colección de cadenas. | Evento Player.StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Evento StringCollectionChange Reproductor de Windows Media
- StringCollectionChange event Reproductor de Windows Media , Player (Clase)
- Clase player Reproductor de Windows Media evento , StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068353"
---
# <a name="playerstringcollectionchange-event"></a>Evento Player.StringCollectionChange

El evento StringCollectionChange tiene lugar cuando cambia una colección de cadenas.

## <a name="syntax"></a>Sintaxis


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdispStringCollection* 
</dt> <dd>

**Objeto StringCollection** que ha cambiado.

</dd> <dt>

*change* 
</dt> <dd>

Número (long) que indica el tipo de cambio que se produjo en la colección de cadenas. Incluye uno de los siguientes valores.



| Number | Descripción                        |
|--------|------------------------------------|
| 0      | Desconocido. (No es un valor válido)       |
| 1      | Se insertó un elemento.              |
| 2      | La colección de cadenas ha cambiado.     |
| 3      | Se eliminó un elemento.               |
| 4      | Se ha borrado la colección de cadenas. |
| 5      | Las actualizaciones masivas comienzan.        |
| 6      | Las actualizaciones masivas han finalizado.           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Número (long) que contiene el índice del elemento de colección de cadenas que ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





