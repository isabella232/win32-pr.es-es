---
title: TCM_GETITEMRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166254"
---
# <a name="tcm_getitemrect-message"></a>Mensaje \_ GETITEMRECT de TCM

Recupera el rectángulo delimitador de una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador de la pestaña, en coordenadas de ventanilla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

