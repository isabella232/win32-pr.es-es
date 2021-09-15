---
title: WM_GETHOTKEY mensaje (Winuser.h)
description: Se envía para determinar la tecla de acceso activa asociada a una ventana.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- WM_GETHOTKEY entrada de teclado y mouse
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468830"
---
# <a name="wm_gethotkey-message"></a>Mensaje \_ GETHOTKEY de WM

Se envía para determinar la tecla de acceso activa asociada a una ventana.


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el código de clave virtual y los modificadores de la clave activa, o **NULL** si no hay ninguna tecla de acceso activa asociada a la ventana. El código de clave virtual está en el byte bajo del valor devuelto y los modificadores están en el byte alto. Los modificadores pueden ser una combinación de las marcas siguientes de CommCtrl.h.



| Código o valor devuelto                                                                                                                                         | Descripción             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**HOTKEYF \_ Alt**</dt> <dt>0x04</dt> </dl>     | tecla ALT<br/>      |
| <dl> <dt>**HOTKEYF \_ Control**</dt> <dt>0x02</dt> </dl> | Tecla CTRL<br/>     |
| <dl> <dt>**HOTKEYF \_ Ext**</dt> <dt>0x08</dt> </dl>     | Clave extendida<br/> |
| <dl> <dt>**HOTKEYF \_ Mayús**</dt> <dt>0x01</dt> </dl>   | Tecla MAYÚS<br/>    |



 

## <a name="remarks"></a>Observaciones

Estas teclas de acceso rápido no están relacionadas con las teclas de acceso rápido establecidas por [**la función RegisterHotKey.**](/windows/win32/api/winuser/nf-winuser-registerhotkey)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

