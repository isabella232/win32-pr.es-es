---
description: Se envía a la función CPlApplet de una Panel de control cuando se cierra la aplicación Panel de control control de la aplicación. La aplicación de control envía el mensaje una vez para cada cuadro de diálogo que admite la aplicación.
title: CPL_STOP mensaje (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468276"
---
# <a name="cpl_stop-message"></a>Mensaje CPL \_ STOP

Se envía a [**la función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una Panel de control cuando se cierra la aplicación Panel de control control de la aplicación. La aplicación de control envía el mensaje una vez para cada cuadro de diálogo que admite la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo.

</dd> <dt>

*lData* 
</dt> <dd>

Valor que la aplicación Panel de control carga en el miembro **lpData** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) para el cuadro de diálogo. La aplicación carga el **miembro lpData** en respuesta al mensaje [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE.**](cpl-newinquire.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Observaciones

En respuesta a este mensaje, una aplicación Panel de control debe realizar la limpieza para el cuadro de diálogo dado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPL \_ EXIT**](cpl-exit.md)
</dt> <dt>

[**CPL \_ GETCOUNT**](cpl-getcount.md)
</dt> </dl>

 

 
