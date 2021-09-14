---
title: Evento Player.ModeChange
description: El evento ModeChange tiene lugar cuando se cambia Reproductor de Windows Media modo de cambio. | Evento Player.ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Evento ModeChange Reproductor de Windows Media
- Evento ModeChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , ModeChange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070965"
---
# <a name="playermodechange-event"></a>Evento Player.ModeChange

El **evento ModeChange** tiene lugar cuando se cambia Reproductor de Windows Media modo de cambio.

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
| bucle    | Toda la secuencia de pistas se reproduce repetidamente. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Valor** booleano que indica el nuevo estado del modo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Configuración.getMode**](settings-getmode.md)
</dt> <dt>

[**Configuración.setMode**](settings-setmode.md)
</dt> </dl>

 

 





