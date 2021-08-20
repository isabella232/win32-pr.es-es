---
title: MCM_GETCALENDARGRIDINFO mensaje (Commctrl.h)
description: Obtiene información sobre una cuadrícula de calendario.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170172"
---
# <a name="mcm_getcalendargridinfo-message"></a>Mensaje \_ GETCALENDARGRIDINFO de MCM

Obtiene información sobre una cuadrícula de calendario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) que contiene información sobre la cuadrícula de calendario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE si** se realiza correctamente; de lo **contrario, FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





