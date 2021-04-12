---
description: Las excepciones pueden iniciarse por hardware o software, y pueden producirse en el modo kernel, así como en el código de modo de usuario. El control de excepciones estructurado proporciona un único mecanismo para controlar las excepciones en modo de kernel y de modo de usuario.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Control de excepciones (control de errores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb44cd294d89be81862c5330dda5b14811add1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152731"
---
# <a name="exception-handling-error-handling"></a>Control de excepciones (control de errores)

Las excepciones pueden iniciarse por hardware o software, y pueden producirse en el modo kernel, así como en el código de modo de usuario. El control de excepciones estructurado proporciona un único mecanismo para controlar las excepciones en modo de kernel y de modo de usuario.

La ejecución de ciertas secuencias de instrucciones puede producir excepciones iniciadas por el hardware. Por ejemplo, el hardware genera una infracción de acceso cuando un proceso intenta leer o escribir en una dirección virtual a la que no tiene el acceso adecuado.

Los eventos que requieren el control de excepciones también pueden producirse durante la ejecución de una rutina de software (por ejemplo, cuando se especifica un valor de parámetro no válido). Cuando esto sucede, un subproceso puede iniciar una excepción explícitamente mediante una llamada a la función [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) . Esta función permite al subproceso que realiza la llamada especificar información que describe la excepción.

Una excepción puede ser continua o no continuada. Se produce una excepción no continuada cuando el evento no es continuo en el hardware o si la continuación no tiene sentido. Una excepción no continuada no finaliza la aplicación. Por lo tanto, es posible que una aplicación pueda detectar la excepción y ejecutarla. Sin embargo, normalmente se produce una excepción no continuada como resultado de una pila dañada u otro problema grave, lo que dificulta la recuperación de la excepción.

 

 
