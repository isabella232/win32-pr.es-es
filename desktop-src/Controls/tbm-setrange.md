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
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166446"
---
# <a name="tbm_setrange-message"></a>Mensaje TBM \_ SETRANGE

Establece el intervalo de posiciones lógicas mínimas y máximas para el control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar la marca. Si este parámetro es **TRUE,** la barra de seguimiento se vuelve a dibujar después de establecer el intervalo. Si este parámetro es **FALSE,** el mensaje establece el intervalo, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la posición mínima del control deslizante y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la posición del control deslizante actual está fuera del nuevo intervalo, el mensaje **TBM \_ SETRANGE** establece la posición del control deslizante en el nuevo valor máximo o mínimo.

Dado que este mensaje toma dos valores enteros de 16 bits sin signo, el intervalo máximo que este mensaje puede especificar es de 0 a 65 535. Para especificar valores de intervalo más grandes, use los [**mensajes \_ TBM SETRANGEMIN**](tbm-setrangemin.md) y [**TBM \_ SETRANGEMAX.**](tbm-setrangemax.md)

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

