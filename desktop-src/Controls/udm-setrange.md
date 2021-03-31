---
title: Mensaje de UDM_SETRANGE (commctrl. h)
description: Establece las posiciones mínima y máxima (intervalo) de un control de flechas.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079551"
---
# <a name="udm_setrange-message"></a>Error de UDM \_ SetRange

Establece las posiciones mínima y máxima (intervalo) de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **breve** que especifica la posición máxima del control de flechas y el valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **Short** que especifica la posición mínima. Ninguna posición puede ser mayor que el valor de MAXVAL de UD \_ o menor que el valor de MINVAL de Ud \_ . Además, la diferencia entre las dos posiciones no puede superar el \_ MAXVAL de Ud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La posición máxima puede ser menor que la posición mínima. Al hacer clic en el botón de flecha arriba, se mueve la posición actual más cerca de la posición máxima y al hacer clic en el botón de flecha abajo se desplaza hacia la posición mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**UDM \_ SetRange**](udm-setrange.md)
</dt> </dl>

 

