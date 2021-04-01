---
title: Mensaje COLOROKSTRING (commdlg. h)
description: Un cuadro de diálogo de color envía el mensaje registrado COLOROKSTRING al procedimiento de enlace, CCHookProc, cuando el usuario selecciona un color y hace clic en el botón Aceptar.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Cuadros de diálogo de mensaje de COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150275"
---
# <a name="colorokstring-message"></a>Mensaje COLOROKSTRING

Un cuadro de diálogo de **color** envía el mensaje registrado **COLOROKSTRING** al procedimiento de enlace, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), cuando el usuario selecciona un color y hace clic en el botón **Aceptar** . El procedimiento de enlace puede aceptar el color y permitir que el cuadro de diálogo se cierre, o bien rechazar el color y forzar que el cuadro de diálogo permanezca abierto.


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**las choosecolor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . El miembro **rgbResult** de esta estructura contiene el valor de color RGB del color seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve cero, el cuadro de diálogo **color** acepta el color seleccionado y se cierra.

Si el procedimiento de enlace devuelve un valor distinto de cero, el cuadro de diálogo de **color** rechaza el color seleccionado y permanece abierto.

## <a name="remarks"></a>Observaciones

El procedimiento de enlace debe especificar la constante **COLOROKSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **COLOROKSTRINGW** (Unicode) y **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LAS CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> </dl>

 

