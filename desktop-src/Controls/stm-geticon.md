---
title: STM_GETICON mensaje (Winuser.h)
description: Una aplicación envía el mensaje GETICON de STM para recuperar un identificador al icono asociado a un control estático que tiene el estilo \_ SS \_ ICON.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON controles de Windows mensaje
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167006"
---
# <a name="stm_geticon-message"></a>Mensaje \_ GETICON de STM

Una aplicación envía el **mensaje \_ GETICON de STM** para recuperar un identificador al icono asociado a un control estático que tiene el estilo SS \_ ICON.

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

El valor devuelto es un identificador del icono o **NULL** si el control estático no tiene ningún icono asociado o si se produjo un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SETICON de STM \_**](stm-seticon.md)
</dt> </dl>

 

 





