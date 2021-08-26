---
title: Evento Player.OpenStateChange
description: El evento OpenStateChange tiene lugar cuando la propiedad openState cambia el valor. | Evento Player.OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Evento OpenStateChange Reproductor de Windows Media
- Evento OpenStateChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , OpenStateChange
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
ms.openlocfilehash: b65436dee60a5207e09a57a39c32dc479ce110e1dafb07a7dbd7cab86e4f0a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003225"
---
# <a name="playeropenstatechange-event"></a>Evento Player.OpenStateChange

El **evento OpenStateChange** tiene lugar cuando la **propiedad openState** cambia el valor.

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

**Number** (**long**) que especifica el nuevo estado abierto. Consulte [openState](player-openstate.md) para obtener una tabla de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Reproductor de Windows Media puede pasar por varios estados abiertos mientras intenta abrir un archivo de red, como buscar el servidor, conectarse al servidor y, por último, abrir el archivo. Este evento se desencadena cada vez que cambia el estado de apertura.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

Reproductor de Windows Media no se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.openState**](player-openstate.md)
</dt> </dl>

 

 





