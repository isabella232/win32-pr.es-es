---
title: WM_CHARTOITEM mensaje (Winuser.h)
description: Enviado por un cuadro de lista con el estilo WANTKEYBOARDINPUT de LBS \_ a su propietario en respuesta a un mensaje CHAR de \_ WM.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3809ae800cfc753925e7c27d87f970ce56c10d90ace7c23e87b46f3e0067fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957534"
---
# <a name="wm_chartoitem-message"></a>Mensaje \_ CHARTOITEM de WM

Enviado por un cuadro de lista con el estilo [**\_ WANTKEYBOARDINPUT de LBS**](list-box-styles.md) a su propietario en respuesta a un [**mensaje CHAR \_ de WM.**](/windows/desktop/inputdev/wm-char)


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el código de carácter de la tecla que el usuario ha presionado. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la posición actual del cursor de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador en el cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la acción que la aplicación realizó en respuesta al mensaje. Un valor devuelto de -1 o -2 indica que la aplicación controló todos los aspectos de la selección del elemento y no requiere ninguna otra acción por parte del cuadro de lista. Un valor devuelto de 0 o superior especifica el índice de base cero de un elemento en el cuadro de lista e indica que el cuadro de lista debe realizar la acción predeterminada para la pulsación de tecla en el elemento especificado.

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve -1.

Solo los cuadros de lista dibujados por el propietario que no tengan el estilo [**\_ HASSTRINGS de LBS**](list-box-styles.md) pueden recibir este mensaje.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **bool** y devolver el valor directamente. Se omite el valor *\_ MSGRESULT* de DWL establecido por la función [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

