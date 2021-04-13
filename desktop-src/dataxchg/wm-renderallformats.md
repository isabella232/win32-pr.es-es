---
title: Mensaje de WM_RENDERALLFORMATS (Winuser. h)
description: Se envía al propietario del portapapeles antes de que se destruya, si el propietario del portapapeles ha retrasado la representación de uno o más formatos del portapapeles.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- Intercambio de datos de mensajes de WM_RENDERALLFORMATS
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
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534941"
---
# <a name="wm_renderallformats-message"></a>Mensaje de RENDERALLFORMATS de WM \_

Se envía al propietario del portapapeles antes de que se destruya, si el propietario del portapapeles ha retrasado la representación de uno o más formatos del portapapeles. Para que el contenido del portapapeles siga estando disponible para otras aplicaciones, el propietario del portapapeles debe representar los datos en todos los formatos que es capaz de generar y colocar los datos en el portapapeles mediante una llamada a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Cuando se responde a un mensaje de **\_ RENDERALLFORMATS de WM** , la aplicación debe llamar a la función [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) y, a continuación, comprobar que sigue siendo el propietario del portapapeles llamando a la función [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

La aplicación debe comprobar que todavía es el propietario del portapapeles después de abrir el portapapeles porque, después de recibir el mensaje de **\_ RENDERALLFORMATS de WM** , pero antes de abrir el portapapeles, es posible que otra aplicación haya abierto y tomado la propiedad del portapapeles, y que los datos de esa aplicación no se sobrescriban.

En la mayoría de los casos, la aplicación no debe llamar a la función [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), ya que al hacerlo se borrarán los formatos del portapapeles que la aplicación ya ha representado.

Cuando se devuelve la aplicación, el sistema quita los formatos no representados de la lista de formatos de Portapapeles disponibles. Para obtener información sobre la representación diferida, consulte [retardo de representación](clipboard-operations.md#delayed-rendering).

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

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**RENDERFORMAT de WM \_**](wm-renderformat.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

