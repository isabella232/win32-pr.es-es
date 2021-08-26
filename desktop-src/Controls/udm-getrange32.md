---
title: UDM_GETRANGE32 mensaje (Commctrl.h)
description: Recupera el intervalo de 32 bits de un control de flechas.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72078327b7a580768321f14c1d512e097561ae3441667497a822dc8a8a28b4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077105"
---
# <a name="udm_getrange32-message"></a>Mensaje \_ GETRANGE32 de UDM

Recupera el intervalo de 32 bits de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a un entero con signo que recibe el límite inferior del intervalo de control hacia abajo. Este parámetro puede ser **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un entero con signo que recibe el límite superior del intervalo de control hacia abajo. Este parámetro puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





