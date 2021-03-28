---
description: Solicita si es aceptable quitar un objeto de datos en el elemento especificado por la estructura SMDATA adjunta.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Mensaje de SMC_SFDDRESTRICTED (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985734"
---
# <a name="smc_sfddrestricted-message"></a>Mensaje de SFDDRESTRICTED de SMC \_

Solicita si es aceptable quitar un objeto de datos en el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDropTarget* 
</dt> <dd>

Dirección de un puntero void que recibe un puntero a la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Establezca este valor en **null** si no desea aceptar el objeto de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devolver S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
