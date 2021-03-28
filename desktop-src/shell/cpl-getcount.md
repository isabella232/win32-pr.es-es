---
description: Se envía a la función CPlApplet de una aplicación del panel de control para recuperar el número de cuadros de diálogo admitidos por la aplicación.
title: Mensaje de CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540547"
---
# <a name="cpl_getcount-message"></a>CPL \_ mensaje GETCOUNT

Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para recuperar el número de cuadros de diálogo admitidos por la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) devuelve el número de cuadros de diálogo que admite la aplicación del panel de control.

## <a name="remarks"></a>Observaciones

Este mensaje se envía inmediatamente después del mensaje [**CPL \_ init**](cpl-init.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
