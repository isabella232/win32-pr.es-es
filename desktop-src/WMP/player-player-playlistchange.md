---
title: Evento Player.PlaylistChange
description: El evento PlaylistChange tiene lugar cuando cambia una lista de reproducción. | Evento Player.PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Lista de reproducciónCambiar evento Reproductor de Windows Media
- Evento PlaylistChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , PlaylistChange
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
ms.openlocfilehash: 3ff4c45449c8de2062aa53ce9bda89c8d634dd30bc1ac8c03f091e8b97e9ce60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572808"
---
# <a name="playerplaylistchange-event"></a>Evento Player.PlaylistChange

El **evento PlaylistChange** tiene lugar cuando cambia una lista de reproducción.

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

**Objeto de** lista de reproducción que ha cambiado.

</dd> <dt>

*change* 
</dt> <dd>

**Number** ( long )**que** indica el tipo de cambio que se produjo en la lista de reproducción. Contiene uno de los valores siguientes.



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
| 8      | NameChange    |
| 9      | No compatible |
| 10     | Sort          |



 

La constante de enumeración de estilo C se puede derivar prefindo el valor de nombre con "wmplc". Por ejemplo, la constante para el estado Move es **wmplcMove**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





