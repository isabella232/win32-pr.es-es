---
title: WM_RENDERALLFORMATS mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles antes de que se destruya, si el propietario del Portapapeles ha retrasado la representación de uno o varios formatos del Portapapeles.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77dae9b44cb379ed62c99c601d308fdec500440a9ebad0ffeaffad16ec780dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636065"
---
# <a name="wm_renderallformats-message"></a>Mensaje \_ RENDERALLFORMATS de WM

Se envía al propietario del Portapapeles antes de que se destruya, si el propietario del Portapapeles ha retrasado la representación de uno o varios formatos del Portapapeles. Para que el contenido del Portapapeles permanezca disponible para otras aplicaciones, el propietario del Portapapeles debe representar los datos en todos los formatos que pueda generar y colocar los datos en el Portapapeles mediante una llamada a la función [**SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Al responder a un mensaje **\_ RENDERALLFORMATS** de WM, la aplicación debe llamar a la función [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) y, a continuación, comprobar que sigue siendo el propietario del Portapapeles llamando a la función [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

La aplicación debe comprobar que sigue siendo el propietario del Portapapeles después de abrir el Portapapeles porque después de recibir el mensaje **\_ RENDERALLFORMATS** de WM, pero antes de abrir el Portapapeles, es posible que otra aplicación se haya abierto y tomado posesión del Portapapeles, y no se deben sobrescribir los datos de esa aplicación.

En la mayoría de los casos, la aplicación no debe llamar a la función [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), ya que al hacerlo se borrarán los formatos del Portapapeles que la aplicación ya ha representado.

Cuando la aplicación vuelve, el sistema quita los formatos no representadas de la lista de formatos de Portapapeles disponibles. Para obtener información sobre la representación retrasada, vea [Representación retrasada.](clipboard-operations.md#delayed-rendering)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**RENDERFORMAT DE WM \_**](wm-renderformat.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

