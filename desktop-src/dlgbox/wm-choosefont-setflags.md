---
title: WM_CHOOSEFONT_SETFLAGS mensaje (Commdlg.h)
description: Una aplicación envía el mensaje \_ WM CHOOSEFONT SETFLAGS a un cuadro de diálogo Fuente para establecer las \_ opciones de presentación del cuadro de diálogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573049"
---
# <a name="wm_choosefont_setflags-message"></a>Mensaje \_ CHOOSEFONT \_ SETFLAGS de WM

Una aplicación envía el mensaje **\_ WM CHOOSEFONT \_ SETFLAGS** **a** un cuadro de diálogo Fuente para establecer las opciones de presentación del cuadro de diálogo.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que contiene nuevos valores en el **miembro Flags.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La [**función ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea un **cuadro de diálogo Fuente** y usa una estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar los valores iniciales del **miembro Flags.** Use el **mensaje \_ WM CHOOSEFONT \_ SETFLAGS** para especificar valores diferentes para **el miembro Flags** mientras el **cuadro de** diálogo Fuente está abierto.

Normalmente, debe enviar el mensaje **\_ WM CHOOSEFONT \_ SETFLAGS** desde un procedimiento de enlace [**CFHookProc.**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)

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

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

