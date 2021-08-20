---
description: La clase LockIt es una clase interna que bloquea y desbloquea el DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: IMediaObjectImpl::LockIt (Clase, Dmoimpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c541fe73d36c29cf58944ba90a19a439d9c637ff3d378f3f6b0f436910ed0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998184"
---
# <a name="imediaobjectimpllockit-class"></a>IMediaObjectImpl::LockIt (Clase)

La `LockIt` clase es una clase interna que bloquea y desbloquea el DMO.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="p"></span><span id="P"></span>*P*
</dt> <dd>

Puntero al objeto derivado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El `LockIt` constructor bloquea el DMO y el destructor desbloquea el DMO. Para bloquear el objeto desde dentro de la clase derivada, declare una variable local de tipo `LockIt` . El DMO está bloqueado mientras el `LockIt` objeto permanece en el ámbito:


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



Los métodos **de IMediaObjectImpl** bloquean automáticamente el DMO.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dmoimpl.h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Plantilla de clase IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




