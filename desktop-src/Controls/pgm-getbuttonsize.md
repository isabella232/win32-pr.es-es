---
title: PGM_GETBUTTONSIZE mensaje (Commctrl.h)
description: Recupera el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro Pager \_ GetButtonSize.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a77bbfdbac95c10afc721cfbae41798083ea98f4dd78e9dfdec9099871d7afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985905"
---
# <a name="pgm_getbuttonsize-message"></a>Mensaje \_ GETBUTTONSIZE de PGM

Recupera el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ GetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene el tamaño del botón actual, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





