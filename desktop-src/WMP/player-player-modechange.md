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
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054363"
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

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media, y se puede acceder o pasar a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





