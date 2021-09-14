---
title: PGM_GETBORDER mensaje (Commctrl.h)
description: Recupera el tamaño del borde actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la \_ macro Pager GetBorder.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167721"
---
# <a name="pgm_getborder-message"></a>Mensaje \_ GETBORDER de PGM

Recupera el tamaño del borde actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ Pager GetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene el tamaño del borde actual, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PGM \_ SETBORDER**](pgm-setborder.md)
</dt> </dl>

 

 





