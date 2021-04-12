---
description: El modo de error indica al sistema cómo la aplicación va a responder a errores graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152734"
---
# <a name="error-mode"></a>Modo de error

El modo de error indica al sistema cómo la aplicación va a responder a errores graves. Los errores graves incluyen el error de disco, los errores de unidad no preparada, la falta de alineación de los datos y las excepciones no controladas. Este modo de error se puede administrar por subproceso o por proceso. Una aplicación puede permitir que el sistema muestre un cuadro de mensaje que informa al usuario de que se ha producido un error o puede controlar los errores.

Para controlar estos errores sin la intervención del usuario, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) o el [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)específico del subproceso. Después de llamar a una de estas funciones y especificar las marcas apropiadas, el sistema no mostrará los cuadros de mensaje de error correspondientes.

Un proceso puede recuperar su modo de error mediante [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) o [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).

Se recomienda que todas las aplicaciones llamen a la función [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) de todo el proceso con un parámetro de **SEM \_ FAILCRITICALERRORS** en el inicio. Esto es para evitar que los cuadros de diálogo del modo de error bloqueen la aplicación.

Aparte de eso, los autores de las llamadas deberían favorecer las versiones específicas del subproceso de estas funciones, ya que son menos perjudiciales para el comportamiento normal del sistema.

 

 
