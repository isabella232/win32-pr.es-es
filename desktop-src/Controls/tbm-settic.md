---
title: TBM_SETTIC mensaje (Commctrl.h)
description: Establece una marca de graduación en una barra de seguimiento en la posición lógica especificada.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f286a2f03e318629a10651d066da5aa6cfe70aa293f242ad7508d0ef4739a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540025"
---
# <a name="tbm_settic-message"></a>Mensaje \_ TBM SETTIC

Establece una marca de graduación en una barra de seguimiento en la posición lógica especificada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Posición de la marca de graduación. Este parámetro puede ser cualquiera de los valores enteros del intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se establece la marca de graduación o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Una barra de seguimiento crea sus propias marcas de graduación primero y último. No use este mensaje para establecer la primera y la última marca de graduación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





