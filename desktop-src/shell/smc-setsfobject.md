---
description: Le notifica que guarde el objeto que se ha pasado.
title: Mensaje de SMC_SETSFOBJECT (shobjidl. h)
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
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277630"
---
# <a name="smc_setsfobject-message"></a>Mensaje de SETSFOBJECT de SMC \_

Le notifica que guarde el objeto que se ha pasado.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*suscripto* 
</dt> <dd>

IID asociado al objeto.

</dd> <dt>

*FV* 
</dt> <dd>

Puntero a la interfaz en el objeto especificado por *IID*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devolver S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

La notificación de **SMC \_ SETSFOBJECT** se usa con el flujo de IID \_ . El objeto se guarda en un formulario guardado en el registro y no se hace nada con el recuento de referencias en el objeto pasado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




