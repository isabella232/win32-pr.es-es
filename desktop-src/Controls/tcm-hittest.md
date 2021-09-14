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
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166234"
---
# <a name="tcm_hittest-message"></a>Mensaje \_ HITTEST de TCM

Determina qué pestaña, si existe, está en una posición de pantalla especificada. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica la posición de la pantalla que se debe probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la pestaña o -1 si no hay ninguna pestaña en la posición especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





