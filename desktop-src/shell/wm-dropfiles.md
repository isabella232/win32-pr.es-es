---
description: Se envía cuando el usuario coloca un archivo en la ventana de una aplicación que se ha registrado como destinatario de archivos colocados.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Mensaje de WM_DROPFILES (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985394"
---
# <a name="wm_dropfiles-message"></a>Mensaje de DROPFILES de WM \_

Se envía cuando el usuario coloca un archivo en la ventana de una aplicación que se ha registrado como destinatario de archivos colocados.


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDrop* 
</dt> <dd>

Identificador de una estructura interna que describe los archivos colocados. Pase este identificador [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)o [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para recuperar información acerca de los archivos colocados.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

El identificador HDROP se declara en ShellAPI. h. Debe incluir este encabezado en la compilación para usar **WM \_ DROPFILES**. Para obtener más información sobre cómo usar arrastrar y colocar para transferir datos de Shell, consulte transferencia de [datos de Shell mediante arrastrar y colocar o el portapapeles](dragdrop.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
