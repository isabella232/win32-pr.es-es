---
title: LVM_GETFOOTERRECT mensaje (Commctrl.h)
description: Recupera las coordenadas del pie de página para un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetFooterRect.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bc2c5cd724c9b5b4885b99123489e49ead52243d43388e7eb22808fb43a826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411464"
---
# <a name="lvm_getfooterrect-message"></a>Mensaje \_ GETFOOTERRECT de LVM

Recupera las coordenadas del pie de página para un control de vista de lista. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetFooterRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa. Debe ser 0.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas. El proceso de llamada es responsable de asignar esta estructura. Las coordenadas recibidas se expresan como coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

