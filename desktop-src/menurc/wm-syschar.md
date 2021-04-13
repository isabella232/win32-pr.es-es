---
title: Mensaje de WM_SYSCHAR (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando \_ la función TranslateMessage traduce un mensaje de SYSKEYDOWN de WM.
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
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535547"
---
# <a name="wm_syschar-message"></a>Mensaje de SYSCHAR de WM \_

Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje de [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) . Especifica el código de carácter de una tecla de carácter del sistema, que es una tecla de carácter que se presiona mientras la tecla ALT está presionada.


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

El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.



| Bits                                                                             | Significado                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | Número de repeticiones del mensaje actual. El valor es el número de veces que la pulsación de tecla se repitió automáticamente como resultado del usuario que mantiene presionada la tecla. Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes. Sin embargo, el número de repeticiones no es acumulativo.<br/> |
| <dl> <dt>16 23</dt> </dl> | Código de recorrido. El valor depende del fabricante de equipos originales (OEM).<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102. El valor es 1 si es una clave extendida; de lo contrario, es 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Sector No use.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | Código de contexto. El valor es 1 si se mantiene presionada la tecla ALT mientras se presiona la tecla; de lo contrario, el valor es 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | Estado de la clave anterior. El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | Estado de transición. El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.<br/>                                                                                                                                                              |

Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , que lo controlará como si fuera un mensaje de clave estándar en lugar de un mensaje de clave de carácter del sistema. Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco de teclado.

Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. tecla Impr Pant; tecla INTERRUMPIr; tecla Bloq Num; y la división (/) y escriba las teclas en el teclado numérico. Otros teclados pueden admitir el bit extendido-Key en el parámetro.

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**SYSKEYDOWN de WM \_**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

