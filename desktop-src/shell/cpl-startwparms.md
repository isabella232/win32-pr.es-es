---
description: Se envía para notificar a CPlApplet que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. CPlApplet debe mostrar el cuadro de diálogo correspondiente y realizar las tareas especificadas por el usuario.
title: Mensaje de CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000985"
---
# <a name="cpl_startwparms-message"></a>CPL \_ STARTWPARMS Message

Se envía para notificar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. **CPlApplet** debe mostrar el cuadro de diálogo correspondiente y realizar las tareas especificadas por el usuario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Cadena con instrucciones adicionales para la ejecución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se ha controlado el mensaje o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

**CPL \_ STARTWPARMS** es similar a [**CPL \_ DBLCLK**](cpl-dblclk.md) , pero le permite pasar una cadena a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) en lugar de un **int**. Puede utilizar esta cadena como una manera flexible de proporcionar instrucciones detalladas para la ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
