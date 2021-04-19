---
title: Mensaje de WM_CHOOSEFONT_GETLOGFONT (commdlg. h)
description: Una aplicación envía el \_ mensaje de CHOOSEFONT GETLOGFONT de WM \_ a un cuadro de diálogo de fuente para recuperar información sobre las selecciones de fuente actuales del usuario.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695975"
---
# <a name="wm_choosefont_getlogfont-message"></a>\_Mensaje GETLOGFONT de CHOOSEFONT de WM \_

Una aplicación envía el mensaje de **\_ CHOOSEFONT \_ GETLOGFONT de WM** a un cuadro de diálogo de **fuente** para recuperar información sobre las selecciones de fuente actuales del usuario.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recibe información sobre las selecciones de fuente actuales del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea un cuadro de diálogo de **fuente** . Cuando el usuario cierra el cuadro de diálogo **fuente** , la función **ChooseFont** devuelve información sobre las selecciones de fuente del usuario en la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . El miembro **lpLogFont** de la estructura **CHOOSEFONT** es un puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

Use el mensaje de **\_ \_ GETLOGFONT de CHOOSEFONT de WM** para obtener información sobre las selecciones de fuente actuales del usuario mientras el cuadro de diálogo **fuente** está abierto. Por ejemplo, si habilita el botón **aplicar** en el cuadro de diálogo **fuente** , envíe el mensaje para obtener la información de fuente que se va a aplicar a la selección de texto actual.

Normalmente, se habilita un procedimiento de enlace [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para procesar los mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) para el botón **aplicar** . Cuando el usuario hace clic en el botón **aplicar** , el procedimiento de enlace envía el mensaje de **\_ CHOOSEFONT \_ GETLOGFONT de WM** al cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**NDPTECGDI**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

