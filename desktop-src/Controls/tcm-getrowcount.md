---
title: Mensaje de TCM_GETROWCOUNT (commctrl. h)
description: Recupera el número actual de filas de las fichas de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT controles de mensajes de Windows
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
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905547"
---
# <a name="tcm_getrowcount-message"></a>\_Mensaje GETROWCOUNT de TCM

Recupera el número actual de filas de las fichas de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de filas de pestañas.

## <a name="remarks"></a>Observaciones

Solo los controles de ficha que tienen el estilo de [**\_ varias líneas de TCS**](tab-control-styles.md) pueden tener varias filas de pestañas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





