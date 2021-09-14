---
title: Evento Player.KeyPress
description: El evento KeyPress tiene lugar cuando se presiona y se libera una tecla. | Evento Player.KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Registro de eventos de KeyPress Reproductor de Windows Media
- Evento de KeyPress Reproductor de Windows Media , clase Player
- Clase de reproductor Reproductor de Windows Media evento , KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070988"
---
# <a name="playerkeypress-event"></a>Evento Player.KeyPress

El **evento KeyPress** tiene lugar cuando se presiona y se libera una tecla.

## <a name="syntax"></a>Sintaxis


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nKeyAscii* 
</dt> <dd>

**Number** (**int**) que especifica el código ANSI numérico estándar para el carácter.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este evento se produce cuando la pulsación de tecla da como resultado cualquier carácter de teclado imprimible, la tecla CTRL combinada con un carácter del alfabeto estándar o uno de algunos caracteres especiales, y la tecla ENTRAR o RETROCESO.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





