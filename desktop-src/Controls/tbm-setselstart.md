---
title: TBM_SETSELSTART mensaje (Commctrl.h)
description: Establece la posición lógica inicial del intervalo de selección actual en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el estilo TBS \_ ENABLESELRANGE.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166422"
---
# <a name="tbm_setselstart-message"></a>Mensaje TBM \_ SETSELSTART

Establece la posición lógica inicial del intervalo de selección actual en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el [**estilo TBS \_ ENABLESELRANGE.**](trackbar-control-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar la marca. Si este parámetro es **TRUE,** el mensaje vuelve a dibujar la barra de seguimiento después de establecer el intervalo de selección. Si este parámetro es **FALSE,** el mensaje establece el intervalo de selección, pero no vuelve a dibujar la barra de seguimiento.

</dd> <dt>

*lParam* 
</dt> <dd>

Posición inicial del intervalo de selección.

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

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> </dl>

 

 





