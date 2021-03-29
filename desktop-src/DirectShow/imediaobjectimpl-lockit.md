---
description: La clase LockIt es una clase interna que bloquea y desbloquea DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Clase IMediaObjectImpl:: LockIt (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679272"
---
# <a name="imediaobjectimpllockit-class"></a>IMediaObjectImpl:: LockIt (clase)

La `LockIt` clase es una clase interna que bloquea y desbloquea DMO.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="p"></span><span id="P"></span>*m*
</dt> <dd>

Puntero al objeto derivado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El `LockIt` constructor bloquea DMO y el destructor desbloquea el DMO. Para bloquear el objeto desde dentro de la clase derivada, declare una variable local de tipo `LockIt` . DMO está bloqueado mientras el `LockIt` objeto permanece en el ámbito:


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



Los métodos de **IMediaObjectImpl** bloquean automáticamente DMO.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Plantilla de clase IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




