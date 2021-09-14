---
title: PGM_GETPOS mensaje (Commctrl.h)
description: Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o usar la macro Pager \_ GetPos.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167701"
---
# <a name="pgm_getpos-message"></a>Mensaje \_ GETPOS de PGM

Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ GetPos.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene la posición de desplazamiento actual, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





