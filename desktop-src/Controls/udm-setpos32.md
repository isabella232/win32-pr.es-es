---
title: UDM_SETPOS32 mensaje (Commctrl.h)
description: Establece la posición de un control de arriba a abajo con una precisión de 32 bits.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d8dee48c580df72a32bb2072b00cc2dfbdf38b386825d686e8bc8510ba47e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088425"
---
# <a name="udm_setpos32-message"></a>Mensaje \_ SETPOS32 de UDM

Establece la posición de un control de arriba a abajo con una precisión de 32 bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Variable de tipo entero que especifica la nueva posición para el control de arriba a abajo. Si el parámetro está fuera del intervalo especificado del control, *lParam* se establece en el valor válido más cercano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ GETPOS32**](udm-getpos32.md)
</dt> </dl>

 

 





