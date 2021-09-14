---
title: TBM_SETRANGEMIN mensaje (Commctrl.h)
description: Establece la posición lógica mínima del control deslizante en una barra de seguimiento.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166438"
---
# <a name="tbm_setrangemin-message"></a>Mensaje \_ SETRANGEMIN de TBM

Establece la posición lógica mínima del control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vuelva a dibujar la marca. Si este parámetro es **TRUE,** el mensaje vuelve a dibujar la barra de seguimiento después de establecer el intervalo. Si este parámetro es **FALSE**, el mensaje establece el intervalo, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición mínima del control deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la posición del control deslizante actual es menor que el nuevo mínimo, el mensaje **\_ SETRANGEMIN** de TBM establece la posición del control deslizante en el nuevo valor mínimo.

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





