---
title: WM_SYSCHAR mensaje (Winuser.h)
description: Se publica en la ventana con el foco del teclado cuando la función TranslateMessage traduce un mensaje \_ SYSKEYDOWN de WM.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b42d88d5ae1346032da2c663dd8c9189c030d5bb7d538ab7ef84403d42fba76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472093"
---
# <a name="wm_syschar-message"></a>Mensaje \_ SYSCHAR de WM

Se publica en la ventana con el foco del teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**\_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) de WM. Especifica el código de carácter de una tecla de carácter del sistema, es decir, una tecla de carácter que se presiona mientras la tecla ALT está abajo.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de carácter de la tecla de menú de la ventana.

</dd> <dt>

*lParam* 
</dt> <dd>

El recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra en la tabla siguiente.



| Bits                                                                             | Significado                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Recuento de repeticiones para el mensaje actual. El valor es el número de veces que la pulsación de tecla se repitió automáticamente como resultado de que el usuario mantiene presionada la tecla. Si la pulsación de tecla se mantiene lo suficiente, se envían varios mensajes. Sin embargo, el recuento de repeticiones no es acumulativo.<br/> |
| <dl> <dt>16 23</dt> </dl> | Código de examen. El valor depende del fabricante del equipo original (OEM).<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Indica si la tecla es una tecla extendida, como las teclas ALT y CTRL de la derecha que aparecen en un teclado mejorado de 101 o 102 teclas. El valor es 1 si es una clave extendida; De lo contrario, es 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Reservado; no use.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Código de contexto. El valor es 1 si la tecla ALT se mantiene presionada mientras se presiona la tecla . De lo contrario, el valor es 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | Estado de clave anterior. El valor es 1 si la clave está fuera de servicio antes de enviar el mensaje, o es 0 si la clave está arriba.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | Estado de transición. El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.<br/>                                                                                                                                                              |

Para obtener más información, vea [Marcas de mensaje de pulsación de teclas](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator,**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) que lo controlará como si fuera un mensaje de clave estándar en lugar de un mensaje de clave de caracteres del sistema. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco del teclado.

En el caso de los teclados mejorados de 101 y 102 teclas, las teclas extendidas son las teclas ALT y CTRL correctas en la sección principal del teclado. las teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN y arrow de los clústeres situados a la izquierda del teclado numérico; la tecla PRINT SCRN; la clave BREAK; la clave NUMLOCK; y las claves divide (/) y ENTRAR en el teclado numérico. Otros teclados pueden admitir el bit de clave extendida en el parámetro .

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

