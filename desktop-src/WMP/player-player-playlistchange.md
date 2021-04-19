---
title: Evento Player. PlaylistChange
description: El evento PlaylistChange se produce cuando cambia una lista de reproducción. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Media Player PlaylistChange de eventos de Windows
- Evento PlaylistChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708660"
---
# <a name="playerplaylistchange-event"></a>Evento Player. PlaylistChange

El evento **PlaylistChange** se produce cuando cambia una lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Lista de reproducción* 
</dt> <dd>

Objeto de **lista de reproducción** que cambió.

</dd> <dt>

*change* 
</dt> <dd>

**Número** (**largo**) que indica el tipo de cambio que se produjo en la lista de reproducción. Contiene uno de los valores siguientes.



| número | NOMBRE          |
|--------|---------------|
| 0      | Unknown       |
| 1      | Borrar         |
| 2      | InfoChange    |
| 3      | Move          |
| 4      | Eliminar        |
| 5      | Insertar        |
| 6      | Append        |
| 7      | No compatible |
| 8      | NameChange (    |
| 9      | No compatible |
| 10     | Sort          |



 

La constante de enumeración de estilo C se puede derivar prefijando el valor de nombre con "wmplc". Por ejemplo, la constante para el estado de movimiento es **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





