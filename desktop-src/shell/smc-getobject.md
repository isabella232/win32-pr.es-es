---
description: Solicita un puntero a un objeto especificado.
title: Mensaje de SMC_GETOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d0c0592356bff13e60c122b3c88cad05733e4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997789"
---
# <a name="smc_getobject-message"></a>\_Mensaje GETOBJECT de SMC

Solicita un puntero a un objeto especificado.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*suscripto* 
</dt> <dd>

IID asociado al objeto solicitado.

</dd> <dt>

*FV* 
</dt> <dd>

Puntero void que recibe un puntero a la interfaz solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devolver S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación. Cree el objeto solicitado y asigne un puntero a la interfaz solicitada a *PV*.

Se pueden solicitar las siguientes interfaces.

-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
