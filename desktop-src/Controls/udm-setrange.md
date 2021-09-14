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
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165469"
---
# <a name="udm_setrange-message"></a>Mensaje \_ SETRANGE de UDM

Establece las posiciones mínima y máxima (intervalo) de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD es un **valor short** que especifica la posición máxima para el control de arriba **a** abajo, y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor [**short**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) que especifica la posición mínima. Ninguna posición puede ser mayor que el valor MAXVAL de UD \_ o menor que el valor DE UD \_ MINVAL. Además, la diferencia entre las dos posiciones no puede superar LA \_ UD MAXVAL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La posición máxima puede ser menor que la posición mínima. Al hacer clic en el botón de flecha arriba, la posición actual se acerca a la posición máxima y, al hacer clic en el botón de flecha hacia abajo, se desplaza hacia la posición mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM \_ SETRANGE**](udm-setrange.md)
</dt> </dl>

 

