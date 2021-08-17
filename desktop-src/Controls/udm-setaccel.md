---
title: UDM_SETACCEL mensaje (Commctrl.h)
description: Establece la aceleración de un control de arriba a abajo.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL controles de Windows mensaje
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
ms.openlocfilehash: bc746e33c14de0dd177ecc31fc237be7cb8be36280bb2a5ceadff31d2b286ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957744"
---
# <a name="udm_setaccel-message"></a>Mensaje \_ SETACCEL de UDM

Establece la aceleración de un control de arriba a abajo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de [**estructuras UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) especificadas por *aAccels*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**estructuras UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que contienen información de aceleración. Los elementos deben ordenarse en orden ascendente en función del **miembro nSec.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





