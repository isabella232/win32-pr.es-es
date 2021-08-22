---
description: Se envía a una aplicación cuando el IME obtiene un carácter del resultado de la conversión. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: WM_IME_CHAR mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337ca982cbd755e01f3dfab465d8b82948dfdbf053a4a7c03417a1d508bc42d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146788"
---
# <a name="wm_ime_char-message"></a>Mensaje DE \_ CHAR de WM IME \_

Se envía a una aplicación cuando el IME obtiene un carácter del resultado de la conversión. Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Valor de carácter de un solo byte o de doble byte. Para un carácter de doble byte, (BYTE)(wParam >> 8) contiene el byte inicial. Tenga en cuenta que los paréntesis son necesarios porque el operador de conversión tiene mayor prioridad que el operador de desplazamiento.

**Unicode:** Valor de carácter Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Recuento de repeticiones, código de examen, marca de clave extendida, código de contexto, marca de estado de clave anterior y marca de estado de transición, con valores como se define a continuación.



| bit   | Significado                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Recuento de repeticiones. Puesto que el primer byte y el segundo byte son continuos, siempre es 1. |
| 16-23 | Buscar un carácter asiático completo en el código.                                            |
| 24    | Clave extendida.                                                                        |
| 25-28 | No se usa.                                                                            |
| 29    | Código de contexto.                                                                        |
| 30    | Estado de clave anterior.                                                                  |
| 31    | Estado de transición.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

A diferencia [**del \_ mensaje WM CHAR**](../inputdev/wm-char.md) para una ventana que no es Unicode, este mensaje puede incluir valores de caracteres de doble byte y de byte único. Para una ventana Unicode, este mensaje es el mismo que WM \_ CHAR.

En el caso de una ventana que no sea Unicode, si el mensaje WM IME CHAR incluye un carácter de doble byte y la aplicación pasa este mensaje \_ \_ a [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)el IME convierte este mensaje en dos mensajes WM CHAR, cada uno con un byte del carácter de doble \_ byte.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del Administrador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
