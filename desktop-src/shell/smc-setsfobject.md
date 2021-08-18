---
description: Le notifica que guarde el objeto pasado.
title: SMC_SETSFOBJECT mensaje (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4ac46fd69d4d91870dcd288190baac275b37a5f093b87646c17d19e479bd710e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968014"
---
# <a name="smc_setsfobject-message"></a>Mensaje SMC \_ SETSFOBJECT

Le notifica que guarde el objeto pasado.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iid* 
</dt> <dd>

El IID asociado al objeto .

</dd> <dt>

*Pv* 
</dt> <dd>

Puntero a la interfaz del objeto especificado por *iid*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El método [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

La **notificación \_ SETSFOBJECT** de SMC se usa con IID \_ Stream. El objeto se guarda en un formulario persistente en el Registro y no se hace nada con el recuento de referencias en el objeto pasado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




