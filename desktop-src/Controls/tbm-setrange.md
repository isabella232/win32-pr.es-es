---
title: Mensaje de TBM_SETRANGE (commctrl. h)
description: Establece el intervalo de posiciones lógicas mínima y máxima para el control deslizante en una barra de desplazamiento.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079123"
---
# <a name="tbm_setrange-message"></a>\_Mensaje de SetRange TBM

Establece el intervalo de posiciones lógicas mínima y máxima para el control deslizante en una barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar el marcador. Si este parámetro es **true**, el TrackBar se vuelve a dibujar una vez establecido el intervalo. Si este parámetro es **false**, el mensaje establece el intervalo pero no vuelve a dibujar el TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la posición mínima del control deslizante y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la posición del control deslizante actual está fuera del nuevo intervalo, el mensaje de **\_ SetRange TBM** establece la posición del control deslizante en el nuevo valor máximo o mínimo.

Dado que este mensaje toma valores enteros de 2 16 bits sin signo, el intervalo máximo que puede especificar este mensaje es de 0 a 65.535. Para especificar valores de intervalo mayores, use los mensajes [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) y [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

