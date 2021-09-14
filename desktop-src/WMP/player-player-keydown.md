---
title: Evento Player.KeyDown
description: El evento KeyDown tiene lugar cuando se presiona una tecla. | Evento Player.KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Evento KeyDown Reproductor de Windows Media
- Evento KeyDown Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , KeyDown
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070989"
---
# <a name="playerkeydown-event"></a>Evento Player.KeyDown

El **evento KeyDown** tiene lugar cuando se presiona una tecla.

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

**Number** (**int**) que especifica la tecla física que se presiona. Para los valores posibles, vea la sección Comentarios.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El *argumento nKeyCode* especifica una clave física. En las tablas siguientes se muestran los valores posibles de las teclas principales en un teclado estándar.

Valores de las claves principales.



| Clave                     | Value   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Bloq Mayús               | 20      |
| MAYÚS (izquierda o derecha)   | 16      |
| CTRL (izquierda o derecha)    | 17      |
| ALT (izquierda o derecha)     | 18      |
| SPACE                   | 32      |
| RETROCESO               | 8       |
| ENTRAR                   | 13      |
| Windows de logotipo, izquierda  | 91      |
| Windows de logotipo, derecha | 92      |
| Clave de la aplicación         | 93      |



 

Valores de las teclas de panel numérico.



| Clave               | Value  |
|-------------------|--------|
| 0-9               | 96-105 |
| BLOQUEO NUM          | 144    |
| DIVIDE (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SUBTRACT (-)      | 109    |
| ADD (+)           | 107    |
| SEPARATOR (Entrar) | 108    |
| DECIMAL (.)       | 110    |



 

Valores de las teclas de navegación.



| Clave         | Value |
|-------------|-------|
| INSERT      | 45    |
| DELETE      | 46    |
| INICIO        | 36    |
| FIN         | 35    |
| RE PÁG     | 33    |
| AV PÁG   | 34    |
| FLECHA ARRIBA    | 38    |
| FLECHA ABAJO  | 40    |
| FLECHA IZQUIERDA  | 37    |
| FLECHA DERECHA | 39    |



 

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

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

 

 





