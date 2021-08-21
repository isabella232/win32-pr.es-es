---
title: WM_SYSDEADCHAR mensaje (Winuser.h)
description: Se envía a la ventana con el foco del teclado cuando la función TranslateMessage traduce un mensaje \_ SYSKEYDOWN de WM.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- WM_SYSDEADCHAR entrada de teclado y mouse
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
ms.openlocfilehash: 5e7ddf63ab4643ef59e45a4850a18a9823753c16a59b4519fe099326fe071704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757227"
---
# <a name="wm_sysdeadchar-message"></a>Mensaje \_ SYSDEADCHAR de WM

Se envía a la ventana con el foco del teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**\_ SYSKEYDOWN**](wm-syskeydown.md) de WM. **WM \_ SYSDEADCHAR especifica** el código de carácter de una tecla de error del sistema, es decir, una tecla fallida que se presiona mientras se mantiene presionada la tecla ALT.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter generado por la tecla de error del sistema, es decir, una tecla fallida que se presiona mientras se mantiene presionada la tecla ALT.

</dd> <dt>

*lParam* 
</dt> <dd>

El recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra en la tabla siguiente.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que la pulsación de tecla se carga de forma automática como resultado de que el usuario mantiene presionada la tecla. Si la pulsación de tecla se mantiene lo suficientemente larga, se envían varios mensajes. Sin embargo, el recuento de repeticiones no es acumulativo. |
| 16-23 | Código de examen. El valor depende del OEM.                                                                                                                                                                                                                          |
| 24    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; de lo contrario, es 0.                                                              |
| 25-28 | Reservado; no se usan.                                                                                                                                                                                                                                                 |
| 29    | Código de contexto. El valor es 1 si la tecla ALT se mantiene presionada mientras se presiona la tecla . De lo contrario, el valor es 0.                                                                                                                                                     |
| 30    | Estado de la clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es 0 si la clave está arriba.                                                                                                                                                    |
| 31    | Estado de transición. El valor es 1 si se va a liberar la tecla o es 0 si se presiona la tecla .                                                                                                                                                                |

Para obtener más información, vea [Marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Para los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT y CTRL derechas en la sección principal del teclado. las teclas de dirección INS, DEL, HOME, END, PAGE UP, PAGE DOWN y en los clústeres situados a la izquierda del teclado numérico; y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de tecla extendida en el *parámetro lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ DEADCHAR**](wm-deadchar.md)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

