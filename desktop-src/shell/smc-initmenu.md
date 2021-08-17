---
description: Le notifica que inicialice la banda de menús.
title: SMC_INITMENU mensaje (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f354769ca18c7490e8bcbf9b1aec0d6c30eb2503dfd66c8a9761a2dddf8ad13d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968064"
---
# <a name="smc_initmenu-message"></a>Mensaje \_ INITMENU de SMC

Le notifica que inicialice la banda de menús.


```C++
SMC_INITMENU
            
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El método [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




