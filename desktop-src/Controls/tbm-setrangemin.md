---
title: Mensaje de TBM_SETRANGEMIN (commctrl. h)
description: Establece la posición lógica mínima para el control deslizante en una barra de desplazamiento.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995925"
---
# <a name="tbm_setrangemin-message"></a>TBM \_ SETRANGEMIN

Establece la posición lógica mínima para el control deslizante en una barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar el marcador. Si este parámetro es **true**, el mensaje vuelve a dibujar el TrackBar una vez establecido el intervalo. Si este parámetro es **false**, el mensaje establece el intervalo pero no vuelve a dibujar el TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición mínima del control deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la posición del control deslizante actual es menor que el mínimo, el mensaje **TBM \_ SETRANGEMIN** establece la posición del control deslizante en el nuevo valor mínimo.

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

[**TBM \_ SetRange**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





