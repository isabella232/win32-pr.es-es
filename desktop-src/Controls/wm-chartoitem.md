---
title: Mensaje de WM_CHARTOITEM (Winuser. h)
description: Se envía mediante un cuadro de lista con el \_ estilo lb WANTKEYBOARDINPUT a su propietario en respuesta a un mensaje de tipo char de WM \_ .
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM controles de mensajes de Windows
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
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104362382"
---
# <a name="wm_chartoitem-message"></a>Mensaje de CHARTOITEM de WM \_

Se envía mediante un cuadro de lista con el estilo [**lb \_ WANTKEYBOARDINPUT**](list-box-styles.md) a su propietario en respuesta a un mensaje de tipo [**\_ Char de WM**](/windows/desktop/inputdev/wm-char) .


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el código de carácter de la tecla que el usuario presionó. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del símbolo de intercalación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica la acción que la aplicación realizó en respuesta al mensaje. Un valor devuelto de-1 o-2 indica que la aplicación controló todos los aspectos de la selección del elemento y no requiere ninguna otra acción por parte del cuadro de lista. Un valor devuelto de 0 o superior especifica el índice de base cero de un elemento del cuadro de lista e indica que el cuadro de lista debe realizar la acción predeterminada para la pulsación de tecla en el elemento especificado.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve-1.

Solo los cuadros de lista dibujados por el propietario que no tienen el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) pueden recibir este mensaje.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente. Se omite el valor de *DWL \_ MSGRESULT* establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

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

[**VKEYTOITEM de WM \_**](wm-vkeytoitem.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**carácter de WM \_**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

