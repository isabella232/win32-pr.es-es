---
title: Mensaje de PGM_GETPOS (commctrl. h)
description: Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro getPos de buscapersonas \_ .
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658258"
---
# <a name="pgm_getpos-message"></a>\_Mensaje GETPOS PGM

Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ getPos de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que contiene la posición de desplazamiento actual, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





