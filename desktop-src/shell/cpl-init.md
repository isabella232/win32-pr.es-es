---
description: Se envía a la función CPlApplet de una aplicación del panel de control para solicitarle que realice una inicialización global, especialmente la asignación de memoria.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Mensaje de CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984338"
---
# <a name="cpl_init-message"></a>CPL \_ mensaje init

Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para solicitarle que realice una inicialización global, especialmente la asignación de memoria.


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

Si la inicialización se realiza correctamente, la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) debe devolver un valor distinto de cero. De lo contrario, debe devolver cero.

Si [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) devuelve cero, la aplicación de control finaliza la comunicación y libera el archivo DLL que contiene la aplicación del panel de control.

## <a name="remarks"></a>Observaciones

Dado que esta es la única manera en que una aplicación del panel de control puede indicar una condición de error, la aplicación debe asignar memoria en respuesta a este mensaje.

Este mensaje se envía inmediatamente después de que se cargue el archivo DLL que contiene la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
