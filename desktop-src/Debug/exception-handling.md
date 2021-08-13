---
description: Las excepciones se pueden iniciar mediante hardware o software, y pueden producirse en modo kernel, así como en código en modo de usuario. El control estructurado de excepciones proporciona un único mecanismo para el control de excepciones en modo kernel y en modo de usuario.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Control de excepciones (control de errores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253776619100095ae1ba9c92fa2caa373bc950bdf6725c6ef5d0239520320bd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260875"
---
# <a name="exception-handling-error-handling"></a>Control de excepciones (control de errores)

Las excepciones se pueden iniciar mediante hardware o software, y pueden producirse en modo kernel, así como en código en modo de usuario. El control estructurado de excepciones proporciona un único mecanismo para el control de excepciones en modo kernel y en modo de usuario.

La ejecución de determinadas secuencias de instrucciones puede dar lugar a excepciones iniciadas por hardware. Por ejemplo, el hardware genera una infracción de acceso cuando un proceso intenta leer o escribir en una dirección virtual a la que no tiene el acceso adecuado.

Los eventos que requieren control de excepciones también pueden producirse durante la ejecución de una rutina de software (por ejemplo, cuando se especifica un valor de parámetro no válido). Cuando esto sucede, un subproceso puede iniciar una excepción explícitamente llamando a la [**función RaiseException.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) Esta función permite al subproceso que realiza la llamada especificar información que describe la excepción.

Una excepción puede ser continuable o no respetable. Se produce una excepción no pertinente cuando el evento no es continuable en el hardware o si la continuación no tiene sentido. Una excepción no pertinente no finaliza la aplicación. Por lo tanto, es posible que una aplicación pueda detectar la excepción y ejecutarla. Sin embargo, normalmente se produce una excepción no pertinente como resultado de una pila dañada u otro problema grave, lo que dificulta la recuperación de la excepción.

 

 
