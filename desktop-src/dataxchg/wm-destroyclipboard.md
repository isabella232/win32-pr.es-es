---
title: WM_DESTROYCLIPBOARD mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles cuando una llamada a la función EmptyClipboard vacía el Portapapeles. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- WM_DESTROYCLIPBOARD mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466100"
---
# <a name="wm_destroyclipboard-message"></a>Mensaje \_ WM DESTROYCLIPBOARD

Se envía al propietario del Portapapeles cuando una llamada a la [**función EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) vacía el Portapapeles.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_DESTROYCLIPBOARD             0x0307
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

Si una aplicación procesa este mensaje, debe devolver cero.

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

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

