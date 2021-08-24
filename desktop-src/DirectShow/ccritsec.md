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
ms.openlocfilehash: eb57004935a85392057120c0ec369d19217148780079ab4be83088dd3de3ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872196"
---
# <a name="ccritsec-class"></a>CCritSec (clase)

La **clase CCritSec** proporciona un bloqueo de subproceso.

Esta clase es un contenedor fino para un Windows **objeto CRITICAL \_ SECTION.** Puede bloquear y desbloquear el subproceso llamando a los [**métodos CCritSec::Lock**](ccritsec-lock.md) y [**CCritSec::Unlock.**](ccritsec-unlock.md) Sin embargo, es más seguro usar esta clase junto con la [**clase CAutoLock.**](cautolock.md) Cuando la **clase CAutoLock** sale del ámbito, desbloquea automáticamente el **objeto CCritSec.** Además, se compila para un código en línea eficaz.



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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de sección críticos](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[DirectShow Referencia de clase base](base-class-reference.md)
</dt> </dl>

 

