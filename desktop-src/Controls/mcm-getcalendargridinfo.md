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
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072300"
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

**TRUE si** se realiza correctamente; en caso **contrario, FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





