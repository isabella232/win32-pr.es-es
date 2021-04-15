---
title: Evento Player. ModeChange
description: El evento ModeChange se produce cuando se cambia un modo de Media Player de Windows. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Media Player ModeChange de eventos de Windows
- Evento ModeChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708271"
---
# <a name="playermodechange-event"></a>Evento Player. ModeChange

El evento **ModeChange** se produce cuando se cambia un modo de Media Player de Windows.

## <a name="syntax"></a>Sintaxis


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ModeName* 
</dt> <dd>

**Cadena** que indica el modo que se cambió. Contiene uno de los valores siguientes.



| Value   | Descripción                                         |
|---------|-----------------------------------------------------|
| shuffle | Las pistas se reproducen en orden aleatorio.                  |
| bucle    | Toda la secuencia de pistas se reproduce varias veces. |



 

</dd> <dt>

*Nuevovalor* 
</dt> <dd>

**Valor booleano** que indica el nuevo estado del modo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Settings. getMode**](settings-getmode.md)
</dt> <dt>

[**Settings. setMode**](settings-setmode.md)
</dt> </dl>

 

 





