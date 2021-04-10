---
title: Mensaje de DTM_GETIDEALSIZE (commctrl. h)
description: Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la macro GetIdealSize de fecha y hora \_ .
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274514"
---
# <a name="dtm_getidealsize-message"></a>DTM \_ GETIDEALSIZE

Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la [**macro \_ GetIdealSize de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza. Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) para recibir el tamaño ideal. La aplicación que realiza la llamada es responsable de la asignación de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

