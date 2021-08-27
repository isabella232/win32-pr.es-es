---
title: TBM_SETRANGE mensaje (Commctrl.h)
description: Establece el intervalo de posiciones lógicas mínimas y máximas para el control deslizante en una barra de seguimiento.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcd4bf71cfcbc36e098bc83568bdf519209ec82cc9889b6b5ec3934d349f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061145"
---
# <a name="tbm_setrange-message"></a>Mensaje \_ SETRANGE de TBM

Establece el intervalo de posiciones lógicas mínimas y máximas para el control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vuelva a dibujar la marca. Si este parámetro es **TRUE**, la barra de seguimiento se vuelve a dibujar después de establecer el intervalo. Si este parámetro es **FALSE**, el mensaje establece el intervalo, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la posición mínima del control deslizante y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la posición del control deslizante actual está fuera del nuevo intervalo, el mensaje **\_ SETRANGE** de TBM establece la posición del control deslizante en el nuevo valor máximo o mínimo.

Dado que este mensaje toma dos valores enteros de 16 bits sin signo, el intervalo máximo que este mensaje puede especificar es de 0 a 65 535. Para especificar valores de intervalo mayores, use los [**mensajes TBM \_ SETRANGEMIN**](tbm-setrangemin.md) y [**TBM \_ SETRANGEMAX.**](tbm-setrangemax.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

