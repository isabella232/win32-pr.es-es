---
title: LVM_GETBKIMAGE mensaje (Commctrl.h)
description: Obtiene la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetBkImage.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3393c226c250de2821d7fab930f950ff5a223218a77a1b9c4bc20b51b527a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062645"
---
# <a name="lvm_getbkimage-message"></a>Mensaje \_ GETBKIMAGE de LVM

Obtiene la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetBkImage.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que recibirá la información de la imagen de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETBKIMAGEW** (Unicode) y **LVM \_ GETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVM \_ SETBKIMAGE**](lvm-setbkimage.md)
</dt> </dl>

 

 





