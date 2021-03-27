---
description: Se envía a la función CPlApplet de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.
title: Mensaje de CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f4c75a2610dab9e94a97eb7920c9de43cf44efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153919"
---
# <a name="cpl_inquire-message"></a>CPL \_ mensaje de consulta

Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para solicitar información sobre un cuadro de diálogo que la aplicación admite.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo comprendido entre cero y uno menos que el valor devuelto en respuesta al mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) (CPL \_ getCount – 1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

Dirección de una estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . La aplicación debe rellenar esta estructura con los identificadores de recursos para el icono, el nombre corto, la descripción y cualquier valor definido por el usuario asociado al cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Observaciones

El panel de control envía el mensaje **CPL de \_ consulta** una vez para cada cuadro de diálogo admitido por la aplicación. El panel de control también envía un mensaje [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) para cada cuadro de diálogo. Estos mensajes se envían inmediatamente después del mensaje [**CPL \_ GETCOUNT**](cpl-getcount.md) . Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ inquire** y **CPL \_ NEWINQUIRE** .

Puede realizar la inicialización del cuadro de diálogo cuando reciba **CPL \_ consulta**. Si tiene que asignar memoria, hágalo en respuesta al mensaje [**CPL \_ init**](cpl-init.md) .

El mensaje [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) devuelve información en un formulario que el sistema no puede almacenar en caché. Por esta razón, la mayoría de las funciones de [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deben procesar **CPL \_ inquire** y omitir **CPL \_ NEWINQUIRE**.

Las únicas aplicaciones que deben usar [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo. En este caso, el controlador de CPL de la **\_ consulta** debe especificar el valor de CPL \_ Dynamic \_ res para los miembros **idIcon**, **idName** o **idInfo** de la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , en lugar de especificar un identificador de recursos válido. Esto hace que el panel de control envíe el mensaje **CPL \_ NEWINQUIRE** cada vez que necesite el icono y las cadenas de presentación, lo que le permite especificar información según el estado actual del equipo. Esto es significativamente más lento que el uso de la información almacenada en caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
