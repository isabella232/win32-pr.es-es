---
description: Se envía para notificar a CPlApplet que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. CPlApplet debe mostrar el cuadro de diálogo correspondiente y llevar a cabo las tareas especificadas por el usuario.
title: CPL_STARTWPARMS mensaje (Cpl.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468275"
---
# <a name="cpl_startwparms-message"></a>Mensaje \_ STARTWPARMS de CPL

Se envía para notificar [**a CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. **CPlApplet** debe mostrar el cuadro de diálogo correspondiente y llevar a cabo las tareas especificadas por el usuario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo de cero a uno menos que el valor devuelto en respuesta al mensaje [**\_ GETCOUNT**](cpl-getcount.md) de CPL (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Cadena con instrucciones adicionales para la ejecución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se controló el mensaje o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

**CPL \_ STARTWPARMS es** similar a [**\_ DBLCLK de CPL,**](cpl-dblclk.md) pero permite pasar una cadena a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) en lugar de **a int**. Puede usar esta cadena como una manera flexible de proporcionar instrucciones detalladas para la ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
