---
description: La clase CAutoLock contiene una sección crítica para el ámbito de un bloque de código.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Clase CAutoLock (Wxutil. h)
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
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670821"
---
# <a name="cautolock-class"></a>Clase CAutoLock

La `CAutoLock` clase contiene una sección crítica para el ámbito de un bloque de código.

Esta clase funciona junto con la clase [**CCritSec**](ccritsec.md) , que es un contenedor para los objetos de sección críticos. El `CAutoLock` constructor bloquea la sección crítica y el destructor la desbloquea. Mediante el uso de un `CAutoLock` objeto como variable local, puede bloquear una sección crítica con la garantía de que todas las rutas de acceso de código desbloquearán la sección crítica.

En el ejemplo de código siguiente se muestra cómo utilizar esta clase:


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Los métodos de esta clase no están diseñados para invalidarse.



| Variables de miembro protegidas                 | Descripción                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ Plock**](cautolock-m-plock.md)      | Sección crítica para este bloqueo.                                  |
| Métodos públicos                             | Descripción                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Método de constructor. Bloquea el objeto de sección crítica especificado. |
| [**~ CAutoLock**](cautolock--cautolock.md) | Método de destructor. Desbloquea el objeto de sección crítica.          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




