---
title: TBM_SETSELEND mensaje (Commctrl.h)
description: Establece la posición lógica final del intervalo de selección actual en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el estilo \_ ENABLESELRANGE de TBS.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166426"
---
# <a name="tbm_setselend-message"></a>Mensaje \_ SETELEND de TBM

Establece la posición lógica final del intervalo de selección actual en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el [**estilo \_ ENABLESELRANGE de TBS.**](trackbar-control-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vuelva a dibujar la marca. Si este parámetro es **TRUE,** el mensaje vuelve a dibujar la barra de seguimiento después de establecer el intervalo de selección. Si este parámetro es **FALSE,** el mensaje establece el intervalo de selección, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición lógica final del intervalo de selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

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

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





