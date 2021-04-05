---
title: Mensaje de UDM_SETACCEL (commctrl. h)
description: Establece la aceleración para un control de flechas.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079769"
---
# <a name="udm_setaccel-message"></a>\_Mensaje SETACCEL UDM

Establece la aceleración para un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) especificadas por *aAccels*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que contienen información de aceleración. Los elementos deben ordenarse en orden ascendente según el miembro **nSec** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





