---
title: Mensaje de WM_SETFOCUS (Winuser. h)
description: Se envía a una ventana una vez que ha obtenido el foco de teclado.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Entrada de mouse y teclado de mensaje de WM_SETFOCUS
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492652"
---
# <a name="wm_setfocus-message"></a>Mensaje de SETFOCUS de WM \_

Se envía a una ventana una vez que ha obtenido el foco de teclado.


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que ha perdido el foco de teclado. Este parámetro puede ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Para mostrar un símbolo de intercalación, una aplicación debe llamar a las funciones de símbolo de intercalación apropiadas cuando recibe el mensaje de **\_ SETFOCUS de WM** .

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

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**KILLFOCUS de WM \_**](wm-killfocus.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

