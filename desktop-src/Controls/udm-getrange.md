---
title: Mensaje de UDM_GETRANGE (commctrl. h)
description: Recupera las posiciones mínima y máxima (intervalo) de un control de flechas.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274556"
---
# <a name="udm_getrange-message"></a>\_Mensaje GETRANGE UDM

Recupera las posiciones mínima y máxima (intervalo) de un control de flechas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un valor de 32 bits que contiene las posiciones mínima y máxima. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es la posición máxima del control y el valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es la posición mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

