---
title: TBM_SETSEL mensaje (Commctrl.h)
description: Establece las posiciones inicial y final del intervalo de selección disponible en una barra de seguimiento.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166429"
---
# <a name="tbm_setsel-message"></a>Mensaje TBM \_ SETSEL

Establece las posiciones inicial y final del intervalo de selección disponible en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vuelva a dibujar la marca. Si este parámetro es **TRUE,** el mensaje vuelve a dibujar la barra de seguimiento después de establecer el intervalo de selección. Si este parámetro es **FALSE,** el mensaje establece el intervalo de selección, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la posición lógica inicial del intervalo de selección y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición lógica final.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje se omite si la barra de seguimiento no tiene el [**estilo \_ ENABLESELRANGE de TBS.**](trackbar-control-styles.md)

**TBM \_ SETSEL** permite restringir el puntero solo a una parte del intervalo disponible para la barra de progreso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

