---
title: WM_CHOOSEFONT_SETLOGFONT mensaje (Commdlg.h)
description: Una aplicación envía el mensaje WM CHOOSEFONT SETLOGFONT a un cuadro de diálogo \_ Fuente para establecer la información de fuente lógica \_ actual.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d35c6f54679389b411417e5539382fd322c0873e6dba87fc90efb93b8be7ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503428"
---
# <a name="wm_choosefont_setlogfont-message"></a>Mensaje \_ CHOOSEFONT \_ SETLOGFONT de WM

Una aplicación envía el mensaje **WM \_ CHOOSEFONT \_ SETLOGFONT** a un **cuadro de** diálogo Fuente para establecer la información de fuente lógica actual.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene información sobre la fuente lógica actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Al llamar a la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para crear un cuadro de diálogo **Fuente,** puede usar el miembro **lpLogFont** de la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contenga los valores iniciales del cuadro de diálogo. Use el **mensaje \_ WM CHOOSEFONT \_ SETLOGFONT para** especificar una estructura **LOGFONT** con valores diferentes mientras el **cuadro de** diálogo Fuente está abierto.

Normalmente, enviaría el mensaje **\_ WM CHOOSEFONT \_ SETLOGFONT** desde un procedimiento de enlace [**CFHookProc.**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) El procedimiento de enlace también puede enviar los [**mensajes \_ WM CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) [**y WM \_ CHOOSEFONT \_ SETFLAGS.**](wm-choosefont-setflags.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

