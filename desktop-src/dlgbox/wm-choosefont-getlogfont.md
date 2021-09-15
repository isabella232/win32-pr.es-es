---
title: WM_CHOOSEFONT_GETLOGFONT mensaje (Commdlg.h)
description: Una aplicación envía el mensaje WM CHOOSEFONT GETLOGFONT a un cuadro de diálogo Fuente para recuperar información sobre las selecciones de fuentes \_ \_ actuales del usuario.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360512"
---
# <a name="wm_choosefont_getlogfont-message"></a>Mensaje \_ \_ GETLOGFONT DE WM CHOOSEFONT

Una aplicación envía el mensaje **WM \_ CHOOSEFONT \_ GETLOGFONT** **a** un cuadro de diálogo Fuente para recuperar información sobre las selecciones de fuentes actuales del usuario.


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

Puntero a una [**estructura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recibe información sobre las selecciones de fuentes actuales del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

La [**función ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea un **cuadro de diálogo** Fuente. Cuando el usuario cierra el cuadro de diálogo **Fuente,** la función **ChooseFont** devuelve información sobre las selecciones de fuentes del usuario en la [**estructura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) El **miembro lpLogFont** de la **estructura CHOOSEFONT** es un puntero a una estructura [**LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

Use el **mensaje WM \_ CHOOSEFONT \_ GETLOGFONT** para obtener información sobre las selecciones de fuentes actuales del usuario mientras el **cuadro de** diálogo Fuente está abierto. Por ejemplo, si  habilita el  botón Aplicar en el cuadro de diálogo Fuente, envíe el mensaje para obtener la información de fuente que se va a aplicar a la selección de texto actual.

Normalmente, se habilita un procedimiento [*de enlace CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para procesar mensajes [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para el **botón** Aplicar. Cuando el usuario hace clic en el **botón Aplicar,** el procedimiento de enlace envía el mensaje **WM \_ CHOOSEFONT \_ GETLOGFONT** al cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

