---
title: LVM_SETBKIMAGE mensaje (Commctrl.h)
description: Establece la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetBkImage.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE controles de Windows mensaje
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
ms.openlocfilehash: 4f00fbf02d4e354115c01af637251782adb9f95b11923d12cba4bc9f1a0f9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919975"
---
# <a name="lvm_setbkimage-message"></a>Mensaje \_ LVM SETBKIMAGE

Establece la imagen de fondo en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetBkImage.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) que contiene la nueva información de imagen de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario. Devuelve cero si el **miembro ulFlags** de la [**estructura LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) es **LVBKIF \_ SOURCE \_ NONE**.

## <a name="remarks"></a>Comentarios

Dado que el control de vista de lista usa OLE COM para manipular las imágenes de fondo, la aplicación que realiza la llamada debe llamar a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de enviar este mensaje. Es mejor llamar a una de estas funciones cuando se inicializa la aplicación y llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) o [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) cuando la aplicación finaliza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETBKIMAGEW** (Unicode) y **LVM \_ SETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVM \_ GETBKIMAGE**](lvm-getbkimage.md)
</dt> </dl>

 

