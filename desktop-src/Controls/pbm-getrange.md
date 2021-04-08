---
title: Mensaje de PBM_GETRANGE (commctrl. h)
description: Recupera información sobre los límites máximo y mínimo actuales de un control de barra de progreso determinado.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996738"
---
# <a name="pbm_getrange-message"></a>Mensaje de GETRANGE de PBM \_

Recupera información sobre los límites máximo y mínimo actuales de un control de barra de progreso determinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de marca que especifica el valor de límite que se va a usar como valor devuelto del mensaje. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                    | Significado                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Devuelve el límite inferior.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Devuelve el límite superior.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que se va a rellenar con los límites máximo y mínimo del control de barra de progreso. Si este parámetro se establece en **null**, el control devolverá solo el límite especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el valor de límite especificado por *wParam*. Si *lParam* no es **null**, *lParam* debe apuntar a una estructura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que se va a rellenar con ambos valores de límite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





