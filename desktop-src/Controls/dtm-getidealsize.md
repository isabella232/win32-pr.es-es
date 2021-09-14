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
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892353"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

