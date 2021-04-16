---
description: La clase CCritSec proporciona un bloqueo de subprocesos.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Clase CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679400"
---
# <a name="ccritsec-class"></a>Clase CCritSec

La clase **CCritSec** proporciona un bloqueo de subprocesos.

Esta clase es un contenedor fino para un objeto **de \_ sección crítica** de Windows. Puede bloquear y desbloquear el subproceso llamando a los métodos [**CCritSec:: Lock**](ccritsec-lock.md) y [**CCritSec:: Unlock**](ccritsec-unlock.md) . Sin embargo, es más seguro usar esta clase junto con la clase [**CAutoLock**](cautolock.md) . Cuando la clase **CAutoLock** sale del ámbito, desbloquea automáticamente el objeto **CCritSec** . Además, se compila en el código en línea eficaz.



| Variables de miembro público                            | Descripción                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentOwner**](ccritsec-m-currentowner.md) | Identificador de subproceso del subproceso propietario.                  |
| [**m \_ lockCount**](ccritsec-m-lockcount.md)       | Número de bloqueos pendientes en este objeto.              |
| [**m \_ fTrace**](ccritsec-m-ftrace.md)             | Valor booleano que especifica si se va a realizar el seguimiento de este bloqueo. |
| Métodos públicos                                     | Descripción                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Método de constructor.                                      |
| [**~ CCritSec**](ccritsec--ccritsec.md)            | Método de destructor.                                       |
| [**Lock**](ccritsec-lock.md)                      | Bloquea el objeto de sección crítica.                       |
| [**Pulsa**](ccritsec-unlock.md)                  | Desbloquea el objeto de sección crítica.                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de sección crítica](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[Referencia de clase base de DirectShow](base-class-reference.md)
</dt> </dl>

 

