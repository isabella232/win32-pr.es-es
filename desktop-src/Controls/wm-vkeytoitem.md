---
title: WM_VKEYTOITEM mensaje (Winuser.h)
description: Enviado por un cuadro de lista con el estilo \_ LBS WANTKEYBOARDINPUT a su propietario en respuesta a un mensaje \_ WM KEYDOWN.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165186"
---
# <a name="wm_vkeytoitem-message"></a>Mensaje \_ VKEYTOITEM de WM

Enviado por un cuadro de lista con el estilo [**\_ LBS WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un [**mensaje WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown)


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el código de clave virtual de la tecla que el usuario ha presionado. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posición actual del cursor de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la acción que la aplicación realizó en respuesta al mensaje. Un valor devuelto de -2 indica que la aplicación controló todos los aspectos de la selección del elemento y no requiere ninguna acción adicional por parte del cuadro de lista. (Vea Comentarios). Un valor devuelto de -1 indica que el cuadro de lista debe realizar la acción predeterminada en respuesta a la pulsación de tecla. Un valor devuelto de 0 o superior especifica el índice de un elemento en el cuadro de lista e indica que el cuadro de lista debe realizar la acción predeterminada para la pulsación de tecla en el elemento especificado.

## <a name="remarks"></a>Observaciones

Un valor devuelto de -2 solo es válido para las claves que el control de cuadro de lista no traduce en caracteres. Si el mensaje [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) se traduce en un mensaje [**\_ CHAR**](/windows/desktop/inputdev/wm-char) de WM y la aplicación procesa el mensaje **\_ VKEYTOITEM** de WM generado como resultado de la pulsación de tecla, el cuadro de lista omite el valor devuelto y realiza el procesamiento predeterminado para ese carácter). **WM \_ Los mensajes KEYDOWN** generados por claves como VK \_ UP, VK DOWN, VK NEXT y VK PREVIOUS no se \_ \_ \_ traducen a **mensajes WM \_ CHAR.** En tales casos, la captura del mensaje **\_ VKEYTOITEM** de WM y la devolución de -2 impide que el cuadro de lista haga el procesamiento predeterminado para esa clave.

Para capturar las claves que generan un mensaje char y hacen un procesamiento especial, la aplicación debe crear subclases en el cuadro de lista, capturar los mensajes [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) y procesar los mensajes correctamente en el procedimiento de subclase.

Los comentarios anteriores se aplican a los cuadros de lista normales que se crean con el estilo [**\_ LBS WANTKEYBOARDINPUT.**](list-box-styles.md) Si el cuadro de lista está dibujado por el propietario, la aplicación debe procesar el [**mensaje \_ CHARTOITEM de WM.**](wm-chartoitem.md)

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve -1.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **un valor BOOL** y devolver el valor directamente. Se omite el valor MSGRESULT de DWL establecido por la función \_ [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ CHARTOITEM**](wm-chartoitem.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

