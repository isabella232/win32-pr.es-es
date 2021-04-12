---
description: Se envía a una aplicación cuando el IME obtiene un carácter del resultado de la conversión. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Mensaje de WM_IME_CHAR (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424044"
---
# <a name="wm_ime_char-message"></a>\_Mensaje de carácter IME de WM \_

Se envía a una aplicación cuando el IME obtiene un carácter del resultado de la conversión. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Un valor de carácter de un solo byte o de doble byte. Para un carácter de doble byte, (BYTE) (wParam >> 8) contiene el byte inicial. Tenga en cuenta que los paréntesis son necesarios porque el operador de conversión tiene mayor precedencia que el operador de desplazamiento.

**Unicode:** Valor de carácter Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

El número de repeticiones, el código de recorrido, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, con valores como se define a continuación.



| bit   | Significado                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones. Dado que el primer byte y el segundo byte son continuos, siempre es 1. |
| 16-23 | Digitalice el código para un carácter asiático completo.                                            |
| 24    | Clave extendida.                                                                        |
| 25-28 | No se utiliza.                                                                            |
| 29    | Código de contexto.                                                                        |
| 30    | Estado de clave anterior.                                                                  |
| 31    | Estado de transición.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

A diferencia del mensaje de tipo [**\_ Char de WM**](../inputdev/wm-char.md) para una ventana no Unicode, este mensaje puede incluir valores de caracteres de doble byte y de un solo byte. En el caso de una ventana Unicode, este mensaje es el mismo que el de WM \_ Char.

En el caso de una ventana no Unicode, si \_ el \_ mensaje de carácter IME IME incluye un carácter de doble byte y la aplicación pasa este mensaje a [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), el IME convierte este mensaje en dos \_ mensajes de WM Char, cada uno con un byte del carácter de doble byte.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del administrador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
