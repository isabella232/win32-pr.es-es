---
description: Se envía a la función CPlApplet de una Panel de control aplicación para solicitarle que realice la inicialización global, especialmente la asignación de memoria.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: CPL_INIT mensaje (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be6acdf58822e6f10f35880a97a7b5bbb9ce0b7bbbf7556b4c18c3f7ad96f72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456375"
---
# <a name="cpl_init-message"></a>Mensaje \_ INIT de CPL

Se envía a la [**función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una Panel de control aplicación para solicitarle que realice la inicialización global, especialmente la asignación de memoria.


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la inicialización se realiza correctamente, [**la función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) debe devolver un valor distinto de cero. De lo contrario, debería devolver cero.

Si [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) devuelve cero, la aplicación de control finaliza la comunicación y libera el archivo DLL que contiene Panel de control aplicación.

## <a name="remarks"></a>Observaciones

Dado que esta es la única manera en que una Panel de control puede indicar una condición de error, la aplicación debe asignar memoria en respuesta a este mensaje.

Este mensaje se envía inmediatamente después de cargar el archivo DLL que contiene la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
