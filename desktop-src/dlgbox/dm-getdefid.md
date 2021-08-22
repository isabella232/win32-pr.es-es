---
title: DM_GETDEFID mensaje (Winuser.h)
description: Recupera el identificador del control de botón de inserción predeterminado para un cuadro de diálogo.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID cuadros de diálogo del mensaje
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6898ed6484a66e1c0d5fa498b0352498c0a57fbe91a74f738e2c6438511aef21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785827"
---
# <a name="dm_getdefid-message"></a>Mensaje \_ GETDEFID de DM

Recupera el identificador del control de botón de inserción predeterminado para un cuadro de diálogo.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
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

Si existe un botón de inserción predeterminado, la palabra de orden superior del valor devuelto contiene el valor **DC \_ HASDEFID** y la palabra de orden bajo contiene el identificador de control. De lo contrario, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

La [**función DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ SETDEFID**](dm-setdefid.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

 





