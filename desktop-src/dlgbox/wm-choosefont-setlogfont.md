---
title: Mensaje de WM_CHOOSEFONT_SETLOGFONT (commdlg. h)
description: Una aplicación envía el \_ mensaje de CHOOSEFONT \_ SETLOGFONT de WM a un cuadro de diálogo de fuente para establecer la información de fuente lógica actual.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT cuadros de diálogo de mensaje
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
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803086"
---
# <a name="wm_choosefont_setlogfont-message"></a>\_Mensaje SETLOGFONT de CHOOSEFONT de WM \_

Una aplicación envía el mensaje de **\_ CHOOSEFONT \_ SETLOGFONT de WM** a un cuadro de diálogo de **fuente** para establecer la información de fuente lógica actual.


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

Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene información sobre la fuente lógica actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Cuando llame a la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para crear un cuadro de diálogo de **fuente** , puede usar el miembro **lpLogFont** de la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contenga valores iniciales para el cuadro de diálogo. Use el **mensaje \_ CHOOSEFONT de \_ SETLOGFONT de WM** para especificar una estructura **LOGFONT** con valores diferentes mientras el cuadro de diálogo **fuente** está abierto.

Normalmente, se enviará el mensaje de **\_ CHOOSEFONT \_ SETLOGFONT de WM** desde un procedimiento de enlace [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) . El procedimiento de enlace también puede enviar los mensajes [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) y [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) .

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

[**\_GETLOGFONT CHOOSEFONT \_ WM**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Biblioteca de cuadros de diálogo comunes](common-dialog-box-library.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**NDPTECGDI**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

