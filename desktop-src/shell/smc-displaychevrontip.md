---
description: Notifica que hay un recuadro informativo que se va a mostrar para el botón de contenido adicional asociado al elemento especificado por la estructura SMDATA correspondiente.
title: Mensaje de SMC_DISPLAYCHEVRONTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497884"
---
# <a name="smc_displaychevrontip-message"></a>Mensaje de DISPLAYCHEVRONTIP de SMC \_

Notifica que hay un recuadro informativo que se va a mostrar para el botón de contenido adicional asociado al elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Vuelva \_ a aceptar para mostrar el recuadro informativo. Devuelve S \_ false para impedir que se muestre el recuadro informativo.

## <a name="remarks"></a>Observaciones

El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




