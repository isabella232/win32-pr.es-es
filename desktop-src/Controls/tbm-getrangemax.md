---
title: TBM_GETRANGEMAX mensaje (Commctrl.h)
description: Recupera la posición máxima del control deslizante en una barra de seguimiento.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- TBM_GETRANGEMAX controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166509"
---
# <a name="tbm_getrangemax-message"></a>Mensaje \_ GETRANGEMAX de TBM

Recupera la posición máxima del control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica la posición máxima en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.

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

[**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





