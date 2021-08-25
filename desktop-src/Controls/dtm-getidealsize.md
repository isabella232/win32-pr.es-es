---
title: DTM_GETIDEALSIZE mensaje (Commctrl.h)
description: Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la macro DateTime \_ GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639fbbb25fbf61695f83b54f106f45ff3dd421f528807120be52edd7031e4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878235"
---
# <a name="dtm_getidealsize-message"></a>Mensaje \_ GETIDEALSIZE de DTM

Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la macro [**DateTime \_ GetIdealSize.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa. Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) para recibir el tamaño ideal. La aplicación que realiza la llamada es responsable de asignar esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

