---
title: Evento Player. KeyPress
description: El evento KeyPress tiene lugar cuando se presiona y se suelta una tecla. | Evento Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Media Player de eventos KeyPress de Windows
- Evento KeyPress Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento KeyPress
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708653"
---
# <a name="playerkeypress-event"></a>Evento Player. KeyPress

El evento **KeyPress** tiene lugar cuando se presiona y se suelta una tecla.

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

**Número** (**int**) que especifica el código ANSI numérico estándar para el carácter.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este evento se produce cuando el resultado de la pulsación de tecla es cualquier carácter imprimible, la tecla CTRL combinada con un carácter del alfabeto estándar o uno de unos pocos caracteres especiales, y la tecla entrar o retroceso.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





