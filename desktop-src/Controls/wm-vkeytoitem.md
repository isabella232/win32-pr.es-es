---
title: Mensaje de WM_VKEYTOITEM (Winuser. h)
description: Enviado por un cuadro de lista con el \_ estilo lb WANTKEYBOARDINPUT a su propietario en respuesta a un \_ mensaje de KEYDOWN de WM.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM controles de mensajes de Windows
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
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104361945"
---
# <a name="wm_vkeytoitem-message"></a>Mensaje de VKEYTOITEM de WM \_

Enviado por un cuadro de lista con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) .


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el código de tecla virtual de la clave que el usuario presionó. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del símbolo de intercalación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la acción que la aplicación realizó en respuesta al mensaje. Un valor devuelto de-2 indica que la aplicación controló todos los aspectos de la selección del elemento y no requiere ninguna acción adicional por parte del cuadro de lista. (Vea la sección comentarios). Un valor devuelto de-1 indica que el cuadro de lista debe realizar la acción predeterminada en respuesta a la pulsación de tecla. Un valor devuelto de 0 o superior especifica el índice de un elemento del cuadro de lista e indica que el cuadro de lista debe realizar la acción predeterminada de la pulsación de tecla en el elemento especificado.

## <a name="remarks"></a>Observaciones

Un valor devuelto de-2 solo es válido para las claves que el control de cuadro de lista no traduce en caracteres. Si el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) se convierte en un mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) y la aplicación procesa el mensaje de **\_ VKEYTOITEM de WM** generado como resultado de la pulsación de tecla, el cuadro de lista omite el valor devuelto y realiza el procesamiento predeterminado para ese carácter. **WM \_** Los mensajes KEYDOWN generados por claves como VK \_ up, VK \_ Down, VK \_ Next y VK \_ Previous no se traducen a mensajes de tipo **\_ Char** . En tales casos, al interceptar el mensaje de **\_ VKEYTOITEM de WM** y devolver-2 se impide que el cuadro de lista realice el procesamiento predeterminado de esa clave.

Para interceptar las claves que generan un mensaje Char y realizar un procesamiento especial, la aplicación debe crear una subclase del cuadro de lista, interceptar los mensajes de tipo [**\_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y de [**WM \_ Char**](/windows/desktop/inputdev/wm-char) y procesar los mensajes correctamente en el procedimiento de la subclase.

Los comentarios anteriores se aplican a los cuadros de lista normales que se crean con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) . Si el cuadro de lista está dibujado por el propietario, la aplicación debe procesar el mensaje de [**\_ CHARTOITEM de WM**](wm-chartoitem.md) .

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve-1.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente. \_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CHARTOITEM de WM \_**](wm-chartoitem.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

