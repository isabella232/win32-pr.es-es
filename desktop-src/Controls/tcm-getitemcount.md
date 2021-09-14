---
title: TCM_GETITEMCOUNT mensaje (Commctrl.h)
description: Recupera el número de pestañas del control de ficha. Puede enviar este mensaje explícitamente o mediante la macro \_ TabCtrl GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166261"
---
# <a name="tcm_getitemcount-message"></a>Mensaje \_ GETITEMCOUNT de TCM

Recupera el número de pestañas del control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TabCtrl GetItemCount.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





