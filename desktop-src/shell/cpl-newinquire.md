---
description: Se envía a la función CPlApplet de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.
title: Mensaje de CPL_NEWINQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984334"
---
# <a name="cpl_newinquire-message"></a>CPL \_ NEWINQUIRE Message

Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).

</dd> <dt>

*lpncpli* 
</dt> <dd>

Dirección de una estructura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . La aplicación del panel de control debe llenar esta estructura con información sobre el cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Observaciones

Para mejorar el rendimiento, la mayoría de las aplicaciones deben omitir **CPL \_ NEWINQUIRE** y procesar el mensaje CPL de la [**\_ consulta**](cpl-inquire.md) en su lugar.

El panel de control envía el mensaje **CPL \_ NEWINQUIRE** una vez para cada cuadro de diálogo admitido por la aplicación. El panel de control también envía un mensaje de [**CPL \_ consulta**](cpl-inquire.md) para cada cuadro de diálogo. Estos mensajes se envían inmediatamente después del mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) . Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ inquire** y **CPL \_ NEWINQUIRE** .

Puede realizar la inicialización del cuadro de diálogo cuando reciba [**CPL \_ consulta**](cpl-inquire.md). Si tiene que asignar memoria, hágalo en respuesta al mensaje [**CPL \_ init**](cpl-init.md) .

[**CPL \_ La consulta**](cpl-inquire.md) es el mensaje preferido. Esto se debe a que **CPL \_ NEWINQUIRE** devuelve información en un formato que el sistema no puede almacenar en caché. Por lo tanto, las aplicaciones que procesan **CPL \_ NEWINQUIRE** se deben cargar cada vez que el panel de control necesite la información, lo que produce una reducción significativa del rendimiento.

Las únicas aplicaciones que deben usar **CPL \_ NEWINQUIRE** son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo. En este caso, el controlador de CPL de la [**\_ consulta**](cpl-inquire.md) debe especificar el valor de CPL \_ Dynamic \_ res para los miembros **idIcon**, **idName** o **idInfo** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , en lugar de especificar un identificador de recursos válido. Esto hace que el panel de control envíe el mensaje **CPL \_ NEWINQUIRE** cada vez que necesite el icono y las cadenas de presentación, lo que le permite especificar información según el estado actual del equipo. Por supuesto, esto es significativamente más lento que el uso de la información almacenada en caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
