---
title: BM_SETSTATE mensaje (Winuser.h)
description: Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera presionado. Puede enviar este mensaje explícitamente o usar la macro \_ Button SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3bb9451041c602541f039afcd85a895af2f02302dc5d55d64fbefb5bc6e3ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921215"
---
# <a name="bm_setstate-message"></a>Mensaje \_ DE BM SETSTATE

Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera presionado. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button SetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **BOOL** que especifica si el botón está resaltado. El valor **TRUE resalta** el botón. Un valor false **quita** cualquier resaltado.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve cero.

## <a name="remarks"></a>Comentarios

El resaltado solo afecta a la apariencia de un botón. No tiene ningún efecto en el estado de comprobación de un botón de radio o casilla.

Un botón se resalta automáticamente cuando el usuario coloca el cursor sobre él y presiona y mantiene presionado el botón izquierdo del mouse. El resaltado se quita cuando el usuario suelta el botón del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





