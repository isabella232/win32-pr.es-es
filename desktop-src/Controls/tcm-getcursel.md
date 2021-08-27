---
title: TCM_GETCURSEL mensaje (Commctrl.h)
description: Determina la pestaña seleccionada actualmente en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl GetCurSel.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6555194972467486789296377b5aaf87ca5520846ec9bf4c03ec345f635b6557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104905"
---
# <a name="tcm_getcursel-message"></a>Mensaje \_ GETCURSEL de TCM

Determina la pestaña seleccionada actualmente en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la pestaña seleccionada si se realiza correctamente o -1 si no se selecciona ninguna pestaña.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





