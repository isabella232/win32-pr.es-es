---
description: Se envía a la función CPlApplet de una Panel de control para recuperar el número de cuadros de diálogo admitidos por la aplicación.
title: CPL_GETCOUNT mensaje (Cpl.h)
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
ms.openlocfilehash: 58f95a62d17ccafd308666a5632a1f7a42ebfda6ca0a54dfb6dfa9d9eda9b684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715485"
---
# <a name="cpl_getcount-message"></a>Mensaje \_ GETCOUNT de CPL

Se envía a la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una Panel de control para recuperar el número de cuadros de diálogo admitidos por la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) devuelve el número de cuadros de diálogo que admite Panel de control aplicación.

## <a name="remarks"></a>Comentarios

Este mensaje se envía inmediatamente después del [**mensaje \_ INIT de CPL.**](cpl-init.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
