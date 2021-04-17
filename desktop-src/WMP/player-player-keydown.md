---
title: Player. KeyDown (evento)
description: El evento KeyDown tiene lugar cuando se presiona una tecla. | Player. KeyDown (evento)
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Media Player de eventos KeyDown de Windows
- Evento KeyDown Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690818"
---
# <a name="playerkeydown-event"></a>Player. KeyDown (evento)

El evento **KeyDown** tiene lugar cuando se presiona una tecla.

## <a name="syntax"></a>Sintaxis


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Número** (**int**) que especifica qué tecla física se presiona. Para los valores posibles, vea la sección Comentarios.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El argumento *nKeyCode* especifica una clave física. En las tablas siguientes se muestran los posibles valores de las claves principales de un teclado estándar.

Valores de las claves principales.



| Clave                     | Value   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Bloq Mayús               | 20      |
| Mayús (izquierda o derecha)   | 16      |
| CTRL (izquierda o derecha)    | 17      |
| ALT (izquierda o derecha)     | 18      |
| SPACE                   | 32      |
| RETROCESO               | 8       |
| ENTRAR                   | 13      |
| Tecla del logotipo de Windows, izquierda  | 91      |
| Tecla del logotipo de Windows, derecha | 92      |
| Clave de la aplicación         | 93      |



 

Valores de las teclas del panel numérico.



| Clave               | Value  |
|-------------------|--------|
| 0-9               | 96-105 |
| BLOQ NUM          | 144    |
| División (/)        | 111    |
| MULTIPLICAr ( \* )     | 106    |
| RESTA (-)      | 109    |
| AGREGAR (+)           | 107    |
| Separador (entrar) | 108    |
| DECIMAL (.)       | 110    |



 

Valores de las teclas de navegación.



| Clave         | Value |
|-------------|-------|
| INSERT      | 45    |
| Delete      | 46    |
| INICIO        | 36    |
| FIN         | 35    |
| RE PÁG     | 33    |
| AV PÁG   | 34    |
| FLECHA ARRIBA    | 38    |
| FLECHA ABAJO  | 40    |
| FLECHA IZQUIERDA  | 37    |
| FLECHA DERECHA | 39    |



 

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

 

 





