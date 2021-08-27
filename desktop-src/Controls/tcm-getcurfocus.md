---
title: TCM_GETCURFOCUS mensaje (Commctrl.h)
description: Devuelve el índice del elemento que tiene el foco en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 694fb64b033d279292a687c39959925a68999c0b232c847bdf6ec6b476c725e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104945"
---
# <a name="tcm_getcurfocus-message"></a>Mensaje \_ GETCURFOCUS de TCM

Devuelve el índice del elemento que tiene el foco en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetCurFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento de ficha que tiene el foco.

## <a name="remarks"></a>Comentarios

El elemento que tiene el foco puede ser diferente del elemento seleccionado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





