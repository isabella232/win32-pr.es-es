---
title: Mensaje de UDM_GETACCEL (commctrl. h)
description: Recupera información de aceleración de un control de flechas.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489628"
---
# <a name="udm_getaccel-message"></a>\_Mensaje GETACCEL UDM

Recupera información de aceleración de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos de la matriz especificada por *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que reciben información de aceleración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de aceleradores establecidos actualmente para el control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 





