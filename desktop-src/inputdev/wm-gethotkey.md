---
title: Mensaje de WM_GETHOTKEY (Winuser. h)
description: Se envía para determinar la tecla de acceso rápido asociada a una ventana.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Entrada de mouse y teclado de mensaje de WM_GETHOTKEY
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490049"
---
# <a name="wm_gethotkey-message"></a>Mensaje de GETHOTKEY de WM \_

Se envía para determinar la tecla de acceso rápido asociada a una ventana.


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el código de tecla virtual y los modificadores de la tecla de acceso rápido, o **null** si no hay ninguna tecla de acceso rápido asociada a la ventana. El código de tecla virtual está en el byte bajo del valor devuelto y los modificadores se encuentran en el byte superior. Los modificadores pueden ser una combinación de las siguientes marcas de CommCtrl. h.



| Código o valor devuelto                                                                                                                                         | Descripción             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>     | tecla ALT<br/>      |
| <dl> <dt>**HOTKEYF \_ CONTROL**</dt> <dt>0x02</dt> </dl> | Tecla CTRL<br/>     |
| <dl> <dt>**HOTKEYF \_ EXT**</dt> <dt>0x08</dt> </dl>     | Clave extendida<br/> |
| <dl> <dt>**HOTKEYF \_ Mayús**</dt> <dt>0x01</dt> </dl>   | Tecla Mayús<br/>    |



 

## <a name="remarks"></a>Observaciones

Estas teclas de acceso directo no están relacionadas con las teclas de acceso rápido establecidas por la función [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**SETHOTKEY de WM \_**](wm-sethotkey.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

