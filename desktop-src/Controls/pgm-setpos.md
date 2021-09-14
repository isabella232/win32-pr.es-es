---
title: PGM_SETPOS mensaje (Commctrl.h)
description: Establece la posición de desplazamiento actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro Pager \_ SetPos.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167681"
---
# <a name="pgm_setpos-message"></a>Mensaje \_ SETPOS de PGM

Establece la posición de desplazamiento actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetPos.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que contiene la nueva posición de desplazamiento, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





