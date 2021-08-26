---
title: TCM_GETROWCOUNT mensaje (Commctrl.h)
description: Recupera el número actual de filas de pestañas en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e67b2ac40834075b31ccf2415a52c96448b8143dde3d6bc67f9c515e1f601a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104875"
---
# <a name="tcm_getrowcount-message"></a>Mensaje \_ GETROWCOUNT de TCM

Recupera el número actual de filas de pestañas en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetRowCount.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de filas de pestañas.

## <a name="remarks"></a>Comentarios

Solo los controles de pestaña que [**tengan el estilo \_ MULTILINE**](tab-control-styles.md) de TCS pueden tener varias filas de pestañas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





