---
description: La clase CAutoLock contiene una sección crítica para el ámbito de un bloque de código.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: CAutoLock (clase, Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b046111e3a7e22fcf9e380fae09bb2d2007a583e49c0507b8e214142505fe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661707"
---
# <a name="cautolock-class"></a>CAutoLock (clase)

La `CAutoLock` clase contiene una sección crítica para el ámbito de un bloque de código.

Esta clase funciona junto con la [**clase CCritSec,**](ccritsec.md) que es un contenedor para objetos de sección críticos. El `CAutoLock` constructor bloquea la sección crítica y el destructor la desbloquea. Mediante el uso de un objeto como variable local, puede bloquear una sección crítica con la garantía de que todas las rutas de acceso de código `CAutoLock` desbloquearán la sección crítica.

En el ejemplo de código siguiente se muestra cómo usar esta clase:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Los métodos de esta clase no están diseñados para reemplazarse.



| Variables de miembro protegido                 | Descripción                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ pLock**](cautolock-m-plock.md)      | Sección crítica para este bloqueo.                                  |
| Métodos públicos                             | Descripción                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Método constructor. Bloquea el objeto de sección crítica especificado. |
| [**~CAutoLock**](cautolock--cautolock.md) | Método destructor. Desbloquea el objeto de sección crítica.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




