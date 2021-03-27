---
description: Le notifica que el menú se contrae.
title: Mensaje de SMC_EXITMENU (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002298"
---
# <a name="smc_exitmenu-message"></a>Mensaje de EXITMENU de SMC \_

Le notifica que el menú se contrae.


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

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



 

 




