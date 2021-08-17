---
description: Le notifica que se va a mostrar una información sobre el botón de contenido adicional asociado al elemento especificado por la estructura SMDATA adjunta.
title: SMC_DISPLAYCHEVRONTIP mensaje (Shobjidl.h)
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
ms.openlocfilehash: f1107af5cd621bafbc1e463101cee2ea57236b9d29844d6183963134b50ce3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968174"
---
# <a name="smc_displaychevrontip-message"></a>Mensaje \_ DISPLAYCHEVRONTIP de SMC

Le notifica que se va a mostrar una información sobre el botón de contenido adicional asociado al elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK para mostrar la información. Devuelve S FALSE para evitar que se muestre \_ la información.

## <a name="remarks"></a>Comentarios

El método [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




