---
title: Mensaje de PBM_GETSTATE (commctrl. h)
description: Obtiene el estado de la barra de progreso.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996737"
---
# <a name="pbm_getstate-message"></a>Mensaje de GETSTATE de PBM \_

Obtiene el estado de la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado actual de la barra de progreso. Uno de los siguientes valores.



| Código devuelto                                                                                 | Descripción             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ normal**</dt> </dl> | En curso.<br/> |
| <dl> <dt>**\_error PBST**</dt> </dl>  | Error.<br/>       |
| <dl> <dt>**PBST en \_ pausa**</dt> </dl> | En pausa.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





