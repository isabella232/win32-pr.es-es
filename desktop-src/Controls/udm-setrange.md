---
title: UDM_SETRANGE mensaje (Commctrl.h)
description: Establece las posiciones mínima y máxima (intervalo) de un control de flechas.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60499c960b7f2e496dc4317229865a8838013fc5d78c194072bee27e761ba4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408068"
---
# <a name="udm_setrange-message"></a>Mensaje \_ SETRANGE de UDM

Establece las posiciones mínima y máxima (intervalo) de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD es un **valor short** que especifica la posición máxima para el control de arriba **a** abajo, y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor short que especifica la posición mínima. [](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Ninguna posición puede ser mayor que el valor MAXVAL de UD \_ o menor que el valor DE UD \_ MINVAL. Además, la diferencia entre las dos posiciones no puede superar LA \_ UD MAXVAL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La posición máxima puede ser menor que la posición mínima. Al hacer clic en el botón de flecha arriba, la posición actual se acerca a la posición máxima y, al hacer clic en el botón de flecha hacia abajo, se desplaza hacia la posición mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM \_ SETRANGE**](udm-setrange.md)
</dt> </dl>

 

