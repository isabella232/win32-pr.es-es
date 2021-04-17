---
title: Evento Player. OpenStateChange
description: El evento OpenStateChange se produce cuando cambia el valor de la propiedad openState. | Evento Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Media Player OpenStateChange de eventos de Windows
- Evento OpenStateChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708661"
---
# <a name="playeropenstatechange-event"></a>Evento Player. OpenStateChange

El evento **OpenStateChange** se produce cuando cambia el valor de la propiedad **openState** .

## <a name="syntax"></a>Sintaxis


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewState* 
</dt> <dd>

**Número** (**largo**) que especifica el nuevo estado abierto. Consulte [openState](player-openstate.md) para obtener una tabla de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Windows Media Player puede pasar por varios Estados abiertos mientras trata de abrir un archivo de red, como localizar el servidor, conectarse al servidor y, por último, abrir el archivo. Este evento se desencadenará cada vez que cambie el estado abierto.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado. Además, no todos los Estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de los Estados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player. openState**](player-openstate.md)
</dt> </dl>

 

 





