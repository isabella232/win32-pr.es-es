---
title: PBM_GETRANGE mensaje (Commctrl.h)
description: Recupera información sobre los límites altos y bajos actuales de un control de barra de progreso determinado.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167777"
---
# <a name="pbm_getrange-message"></a>Mensaje \_ GETRANGE de PBM

Recupera información sobre los límites altos y bajos actuales de un control de barra de progreso determinado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de marca que especifica qué valor de límite se va a usar como valor devuelto del mensaje. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                    | Significado                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE**</dt> </dl>    | Devuelve el límite bajo.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE**</dt> </dl> | Devuelve el límite alto.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que se va a rellenar con los límites altos y bajos del control de barra de progreso. Si este parámetro se establece en **NULL,** el control devolverá solo el límite especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el valor de límite especificado por *wParam.* Si *lParam no* es **NULL,** *lParam* debe apuntar a una [**estructura PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que se va a rellenar con ambos valores de límite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





