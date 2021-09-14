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
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166282"
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

## <a name="remarks"></a>Observaciones

El elemento que tiene el foco puede ser diferente del elemento seleccionado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





