---
title: Mensaje de WM_SYSDEADCHAR (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando \_ la función TranslateMessage traduce un mensaje de SYSKEYDOWN de WM.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- Entrada de mouse y teclado de mensaje de WM_SYSDEADCHAR
topic_type:
- apiref
api_name:
- WM_SYSDEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2052f8ced24ac998a56a4365552fee4bc5e0b21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714621"
---
# <a name="wm_sysdeadchar-message"></a>Mensaje de SYSDEADCHAR de WM \_

Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje de [**\_ SYSKEYDOWN de WM**](wm-syskeydown.md) . **WM \_ SYSDEADCHAR** especifica el código de carácter de una clave muerta del sistema, es decir, una tecla muerta que se presiona mientras mantiene presionada la tecla Alt.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El código de carácter generado por la clave de inactividad del sistema, que es una tecla muerta que se presiona mientras mantiene presionada la tecla ALT.

</dd> <dt>

*lParam* 
</dt> <dd>

El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Número de repeticiones del mensaje actual. El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla. Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes. Sin embargo, el número de repeticiones no es acumulativo. |
| 16-23 | Código de recorrido. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102. El valor es 1 si es una clave extendida; de lo contrario, es 0.                                                              |
| 25-28 | Sector No use.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor es 1 si se mantiene presionada la tecla ALT mientras se presiona la tecla; de lo contrario, el valor es 0.                                                                                                                                                     |
| 30    | Estado de la clave anterior. El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.                                                                                                                                                    |
| 31    | Estado de transición. El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.                                                                                                                                                                |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**DEADCHAR de WM \_**](wm-deadchar.md)
</dt> <dt>

[**SYSKEYDOWN de WM \_**](wm-syskeydown.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

