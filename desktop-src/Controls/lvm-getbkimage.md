---
title: Mensaje de LVM_GETBKIMAGE (commctrl. h)
description: Obtiene la imagen de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetBkImage de ListView.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE controles de mensajes de Windows
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
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801118"
---
# <a name="lvm_getbkimage-message"></a>\_Mensaje GETBKIMAGE LVM

Obtiene la imagen de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetBkImage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que recibirá la información de la imagen de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETBKIMAGEW** (Unicode) y **\_ GETBKIMAGEA de LVM** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETBKIMAGE LVM**](lvm-setbkimage.md)
</dt> </dl>

 

 





