---
description: 'CPL_INQUIRE mensaje: se envía a la función CPlApplet de una aplicación Panel de control para solicitar información sobre un cuadro de diálogo compatible con la aplicación.'
title: CPL_INQUIRE mensaje (Cpl.h)
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
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468286"
---
# <a name="cpl_inquire-message"></a>Mensaje CPL \_ INQUIRE

Se envía a la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una Panel de control para solicitar información sobre un cuadro de diálogo compatible con la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

Número del cuadro de diálogo. Este número debe estar en el intervalo de cero a uno menos que el valor devuelto en respuesta al mensaje [**\_ GETCOUNT**](cpl-getcount.md) de CPL (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

Dirección de una [**estructura CPLINFO.**](/windows/win32/api/cpl/ns-cpl-cplinfo) La aplicación debe rellenar esta estructura con identificadores de recursos para el icono, el nombre corto, la descripción y cualquier valor definido por el usuario asociado al cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa este mensaje correctamente, debe devolver cero.

## <a name="remarks"></a>Observaciones

El Panel de control envía el **mensaje CPL \_ INQUIRE una** vez para cada cuadro de diálogo compatible con la aplicación. El Panel de control también envía un [**mensaje \_ NEWINQUIRE**](cpl-newinquire.md) de CPL para cada cuadro de diálogo. Estos mensajes se envían inmediatamente después del [**mensaje \_ GETCOUNT de CPL.**](cpl-getcount.md) Sin embargo, el sistema no garantiza el orden en el que se envían los mensajes **CPL \_ INQUIRE** y **CPL \_ NEWINQUIRE.**

Puede realizar la inicialización del cuadro de diálogo cuando reciba **CPL \_ INQUIRE**. Si debe asignar memoria, debe hacerlo en respuesta al [**mensaje \_ INIT de CPL.**](cpl-init.md)

El [**mensaje \_ NEWINQUIRE de CPL**](cpl-newinquire.md) devuelve información en un formulario que el sistema no puede almacenar en caché. Por esta razón, la mayoría [**de las funciones de CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deben procesar **CPL \_ INQUIRE** y omitir **CPL \_ NEWINQUIRE**.

Las únicas aplicaciones que deben usar [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) son aquellas que necesitan cambiar su icono o mostrar cadenas en función del estado del equipo. En este caso, el controlador **CPL \_ INQUIRE** debe especificar el valor CPL DYNAMIC RES para los miembros idIcon , idName o idInfo de la estructura \_ \_ [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo)    en lugar de especificar un identificador de recurso válido. Esto hace que el Panel de control envíe el mensaje **\_ NEWINQUIRE** de CPL cada vez que necesite el icono y las cadenas para mostrar, lo que le permite especificar información basada en el estado actual del equipo. Esto es significativamente más lento que usar la información almacenada en caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
