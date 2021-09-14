---
description: La clase CCritSec proporciona un bloqueo de subproceso.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: CCritSec (clase, Wxutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061323"
---
# <a name="ccritsec-class"></a>CCritSec (clase)

La **clase CCritSec** proporciona un bloqueo de subproceso.

Esta clase es un contenedor fino para un Windows **OBJETO CRITICAL \_ SECTION.** Puede bloquear y desbloquear el subproceso llamando a los métodos [**CCritSec::Lock**](ccritsec-lock.md) y [**CCritSec::Unlock.**](ccritsec-unlock.md) Sin embargo, es más seguro usar esta clase junto con la [**clase CAutoLock.**](cautolock.md) Cuando la **clase CAutoLock** sale del ámbito, desbloquea automáticamente el **objeto CCritSec.** Además, se compila en código en línea eficaz.



| Variables de miembro público                            | Descripción                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentOwner**](ccritsec-m-currentowner.md) | Identificador de subproceso del subproceso propietario.                  |
| [**m \_ lockCount**](ccritsec-m-lockcount.md)       | Número de bloqueos pendientes en este objeto.              |
| [**m \_ fTrace**](ccritsec-m-ftrace.md)             | Valor booleano que especifica si se debe hacer un seguimiento de este bloqueo. |
| Métodos públicos                                     | Descripción                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Método constructor.                                      |
| [**~CCritSec**](ccritsec--ccritsec.md)            | Método destructor.                                       |
| [**Lock**](ccritsec-lock.md)                      | Bloquea el objeto de sección crítica.                       |
| [**Desbloquear**](ccritsec-unlock.md)                  | Desbloquea el objeto de sección crítica.                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de sección crítica](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[DirectShow Referencia de clase base](base-class-reference.md)
</dt> </dl>

 

