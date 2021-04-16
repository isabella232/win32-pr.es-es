---
title: Mensaje de TCM_GETCURSEL (commctrl. h)
description: Determina la pestaña seleccionada actualmente en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetCurSel.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL controles de mensajes de Windows
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
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658356"
---
# <a name="tcm_getcursel-message"></a>\_Mensaje GETCURSEL de TCM

Determina la pestaña seleccionada actualmente en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la pestaña seleccionada si se realiza correctamente, o-1 si no hay ninguna pestaña seleccionada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





