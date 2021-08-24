---
title: TB_GETPADDING mensaje (Commctrl.h)
description: Recupera el relleno de un control de barra de herramientas.
ms.assetid: dde0f44d-5d22-4cab-a7f8-48d84b8995d3
keywords:
- TB_GETPADDING controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f342e3322c0db60f46b0de353c2bbd2f6abe28717aa8ee23db8a3a9f26473113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078329"
---
# <a name="tb_getpadding-message"></a>Mensaje \_ GETPADDING de TB

Recupera el relleno de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene el relleno horizontal en la palabra baja y el relleno vertical en la palabra alta, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ SETPADDING**](tb-setpadding.md)
</dt> </dl>

 

 





