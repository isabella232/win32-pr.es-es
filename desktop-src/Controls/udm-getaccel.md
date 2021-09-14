---
title: UDM_GETACCEL mensaje (Commctrl.h)
description: Recupera la información de aceleración de un control de flechas.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165525"
---
# <a name="udm_getaccel-message"></a>Mensaje \_ GETACCEL de UDM

Recupera la información de aceleración de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos de la matriz especificada por *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**estructuras UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que reciben información de aceleración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de aceleradores establecidos actualmente para el control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 





