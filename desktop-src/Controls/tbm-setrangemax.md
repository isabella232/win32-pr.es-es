---
title: TBM_SETRANGEMAX mensaje (Commctrl.h)
description: Establece la posición lógica máxima del control deslizante en una barra de seguimiento.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- TBM_SETRANGEMAX controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166441"
---
# <a name="tbm_setrangemax-message"></a>Mensaje \_ TBM SETRANGEMAX

Establece la posición lógica máxima del control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar la marca. Si este parámetro es **TRUE,** la barra de seguimiento se vuelve a dibujar después de establecer el intervalo. Si este parámetro es **FALSE,** el mensaje establece el intervalo, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición máxima del control deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la posición del control deslizante actual es mayor que el nuevo máximo, el mensaje **\_ TBM SETRANGEMAX** establece la posición del control deslizante en el nuevo valor máximo.

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

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

 





