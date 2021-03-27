---
description: Se envía a la función CPlApplet de una aplicación del panel de control cuando el usuario hace doble clic en el icono de un cuadro de diálogo admitido por la aplicación.
title: Mensaje de CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997229"
---
# <a name="cpl_dblclk-message"></a>CPL \_ DBLCLK Message

Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control cuando el usuario hace doble clic en el icono de un cuadro de diálogo admitido por la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).

</dd> <dt>

*lData* 
</dt> <dd>

Valor que la aplicación del panel de control cargó en el miembro **lpData** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) para el cuadro de diálogo. La aplicación carga el miembro **lpData** como respuesta al mensaje [**CPL \_ inquire**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, el valor devuelto es cero; de lo contrario, es distinto de cero.

## <a name="remarks"></a>Observaciones

En respuesta a este mensaje, una aplicación del panel de control debe mostrar el cuadro de diálogo correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPL \_ Select**](cpl-select.md)
</dt> </dl>

 

 
