---
description: Se envía a la función CPlApplet de una aplicación del panel de control cuando se cierra la aplicación de control del panel de control. La aplicación de control envía el mensaje una vez por cada cuadro de diálogo que admita la aplicación.
title: Mensaje de CPL_STOP (CPL. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984330"
---
# <a name="cpl_stop-message"></a>CPL \_ detener mensaje

Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control cuando se cierra la aplicación de control del panel de control. La aplicación de control envía el mensaje una vez por cada cuadro de diálogo que admita la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo.

</dd> <dt>

*lData* 
</dt> <dd>

Valor que la aplicación del panel de control cargó en el miembro **lpData** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) para el cuadro de diálogo. La aplicación carga el miembro **lpData** como respuesta al mensaje [**CPL \_ inquire**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Observaciones

En respuesta a este mensaje, una aplicación del panel de control debe realizar la limpieza para el cuadro de diálogo especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**salir de CPL \_**](cpl-exit.md)
</dt> <dt>

[**CPL \_ GETCOUNT**](cpl-getcount.md)
</dt> </dl>

 

 
