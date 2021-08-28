---
title: TCM_HITTEST mensaje (Commctrl.h)
description: Determina qué pestaña, si existe, está en una posición de pantalla especificada. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f0e619303300c5d04fc26a4b32009923422aede2a97b8faeb2175297c87d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104836"
---
# <a name="tcm_hittest-message"></a>Mensaje \_ HITTEST de TCM

Determina qué pestaña, si existe, está en una posición de pantalla especificada. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica la posición de pantalla que se debe probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la pestaña o -1 si no hay ninguna pestaña en la posición especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





