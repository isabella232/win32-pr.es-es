---
description: 'CPL_NEWINQUIRE mensaje: se envía a la función CPlApplet de una aplicación Panel de control para solicitar información sobre un cuadro de diálogo compatible con la aplicación.'
title: CPL_NEWINQUIRE mensaje (Cpl.h)
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
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104443"
---
# <a name="cpl_newinquire-message"></a>Mensaje \_ NEWINQUIRE de CPL

Se envía a la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación Panel de control para solicitar información sobre un cuadro de diálogo compatible con la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo de cero a uno menos que el valor devuelto en respuesta al mensaje [**\_ GETCOUNT**](cpl-getcount.md) de CPL (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpncpli* 
</dt> <dd>

Dirección de una [**estructura NEWCPLINFO.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) La Panel de control debe rellenar esta estructura con información sobre el cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Comentarios

Para mejorar el rendimiento, la mayoría de las aplicaciones deben omitir **CPL \_ NEWINQUIRE y** procesar el [**mensaje CPL \_ INQUIRE en**](cpl-inquire.md) su lugar.

El Panel de control envía el **mensaje \_ NEWINQUIRE** de CPL una vez para cada cuadro de diálogo compatible con la aplicación. El Panel de control también envía un [**mensaje CPL \_ INQUIRE**](cpl-inquire.md) para cada cuadro de diálogo. Estos mensajes se envían inmediatamente después del [**mensaje \_ GETCOUNT de CPL.**](cpl-getcount.md) Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ INQUIRE** y **CPL \_ NEWINQUIRE.**

Puede realizar la inicialización del cuadro de diálogo cuando reciba [**CPL \_ INQUIRE**](cpl-inquire.md). Si debe asignar memoria, debe hacerlo en respuesta al [**mensaje \_ INIT de CPL.**](cpl-init.md)

[**CPL \_ INQUIRE**](cpl-inquire.md) es el mensaje preferido. Esto se debe a **que CPL \_ NEWINQUIRE** devuelve información de forma que el sistema no puede almacenar en caché. Por lo tanto, las aplicaciones que procesan **CPL \_ NEWINQUIRE** deben cargarse cada vez que el Panel de control necesita la información, lo que da lugar a una reducción significativa del rendimiento.

Las únicas aplicaciones que deben **usar CPL \_ NEWINQUIRE** son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo. En este caso, el controlador [**CPL \_ INQUIRE**](cpl-inquire.md) debe especificar el valor de CPL DYNAMIC RES para los miembros idIcon , idName o idInfo de la estructura \_ \_ [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo)    en lugar de especificar un identificador de recurso válido. Esto hace que el Panel de control envíe el mensaje **\_ NEWINQUIRE** de CPL cada vez que necesite el icono y las cadenas de presentación, lo que le permite especificar información basada en el estado actual del equipo. Por supuesto, esto es significativamente más lento que usar la información almacenada en caché.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
