---
title: PGM_SETBORDER mensaje (Commctrl.h)
description: Establece el tamaño del borde actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro Pager \_ SetBorder.
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c44433189c9d791aba1d50372176309682c1361c5b0efe31b11aaa99e9b322b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540535"
---
# <a name="pgm_setborder-message"></a>Mensaje \_ SETBORDER de PGM

Establece el tamaño del borde actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo tamaño del borde, en píxeles. Este valor no debe ser mayor que el botón de paginación o menor que cero. Si *lParam* es demasiado grande, el borde se dibujará con el mismo tamaño que el botón. Si *lParam es* negativo, el tamaño del borde se establecerá en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene el tamaño del borde anterior, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





