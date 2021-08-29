---
title: EM_SETWORDBREAKPROCEX mensaje (Richedit.h)
description: Establece el procedimiento de salto de palabras extendido para un control de edición enriquecido.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- EM_SETWORDBREAKPROCEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc56e147c52d89b929a4e7065d4daafc184406247d60d522ef2bf4317097faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062845"
---
# <a name="em_setwordbreakprocex-message"></a>Mensaje \_ EM SETWORDBREAKPROCEX

Establece el procedimiento de salto de palabras extendido para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [*función EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) o **NULL** para usar el procedimiento predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la dirección del procedimiento de salto de palabras extendido anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EditWordBreakProcEx**](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[**EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md)
</dt> </dl>

 

 





