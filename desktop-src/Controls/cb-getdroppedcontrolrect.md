---
title: Mensaje de CB_GETDROPPEDCONTROLRECT (Winuser. h)
description: Una aplicación envía un \_ mensaje CB GETDROPPEDCONTROLRECT para recuperar las coordenadas de pantalla de un cuadro combinado en su estado desplegable.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491225"
---
# <a name="cb_getdroppedcontrolrect-message"></a>\_Mensaje GETDROPPEDCONTROLRECT CB

Una aplicación envía un mensaje **CB \_ GETDROPPEDCONTROLRECT** para recuperar las coordenadas de pantalla de un cuadro combinado en su estado desplegable.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe las coordenadas del cuadro combinado en su estado desplegable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en el mensaje, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

