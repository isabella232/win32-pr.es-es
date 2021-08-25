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
ms.openlocfilehash: a7a056d55d0ec70b3ff3068580c1e9923b363efa15e9ab26bf8aa67f476cc147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046844"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





