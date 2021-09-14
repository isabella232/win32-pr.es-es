---
title: CB_GETDROPPEDCONTROLRECT mensaje (Winuser.h)
description: Una aplicación envía un mensaje CB GETDROPPEDCONTROLRECT para recuperar las coordenadas de pantalla de un cuadro combinado \_ en su estado desplegable.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968736"
---
# <a name="cb_getdroppedcontrolrect-message"></a>Mensaje \_ GETDROPPEDCONTROLRECT de CB

Una aplicación envía un **mensaje CB \_ GETDROPPEDCONTROLRECT para** recuperar las coordenadas de pantalla de un cuadro combinado en su estado desplegable.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe las coordenadas del cuadro combinado en su estado desplegable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en el mensaje, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

