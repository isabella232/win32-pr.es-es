---
title: Mensaje de LVM_SETBKIMAGE (commctrl. h)
description: Establece la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetBkImage de ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491458"
---
# <a name="lvm_setbkimage-message"></a>\_Mensaje SETBKIMAGE LVM

Establece la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetBkImage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que contiene la nueva información de la imagen de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario. Devuelve cero si el miembro **ulFlags** de la estructura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) es **LVBKIF \_ source \_ None**.

## <a name="remarks"></a>Observaciones

Dado que el control de vista de lista utiliza OLE COM para manipular las imágenes de fondo, la aplicación que realiza la llamada debe llamar a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de enviar este mensaje. Es mejor llamar a una de estas funciones cuando se inicializa la aplicación y llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) o [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) cuando la aplicación está finalizando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) y **\_ SETBKIMAGEA de LVM** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETBKIMAGE LVM**](lvm-getbkimage.md)
</dt> </dl>

 

