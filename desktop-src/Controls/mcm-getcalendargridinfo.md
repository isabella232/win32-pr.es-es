---
title: Mensaje de MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtiene información acerca de una cuadrícula de calendario.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804147"
---
# <a name="mcm_getcalendargridinfo-message"></a>Mensaje de MCM \_ GETCALENDARGRIDINFO

Obtiene información acerca de una cuadrícula de calendario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) que contiene información sobre la cuadrícula del calendario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si es correcto; de lo contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





