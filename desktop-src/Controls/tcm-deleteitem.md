---
title: TCM_DELETEITEM mensaje (Commctrl.h)
description: Quita un elemento de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166286"
---
# <a name="tcm_deleteitem-message"></a>Mensaje \_ DELETEITEM de TCM

Quita un elemento de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ DeleteItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se eliminará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





