---
description: Cuando una operación devuelve SUCCESS, la función ha progresado correctamente hasta un punto definido por la API en función por función.
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: El significado de SUCCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae38aa834b3c60107c0245be2c792703a9c038c6e9b96f982e720bf417af58f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126125"
---
# <a name="the-meaning-of-success"></a>El significado de SUCCESS

## <a name="tapi-2x"></a>TAPI 2.x

Cuando una operación devuelve una indicación SUCCESS (ya sea sincrónicamente cuando la función devuelve para operaciones sincrónicas o de forma asincrónica a través de un mensaje [**LINE \_ REPLY**](./line-reply.md) o [**PHONE \_ REPLY**](./phone-reply.md) para las operaciones asincrónicas), se supone que se cumple lo siguiente:

-   La función ha progresado correctamente hasta un punto definido por la API en función de función por función. Una vez alcanzado ese punto, la operación ha finalizado completamente o estará en un estado de modo que los mensajes de estado independiente informarán a la aplicación sobre el progreso posterior.

    Por ejemplo, la implementación de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) de un proveedor de servicios debe devolver SUCCESS no más tarde que cuando la llamada entra en el estado de llamada siguiente. Lo ideal es que el proveedor indique SUCCESS lo antes posible, como cuando la llamada entra en el estado de llamada de tono de marcado (si procede). Una vez que se ha devuelto SUCCESS a la aplicación, los mensajes LINE \_ CALLSTATE informarán a la aplicación sobre el progreso de la llamada. Los proveedores de servicios que retrasan la devolución de la indicación **lineMakeCall** SUCCESS, por ejemplo, hasta que se complete la marcación, deben tener en cuenta que esto coloca a ese proveedor en una desventaja porque la facilidad de uso en el nivel de aplicación puede estar muy limitada. Por ejemplo, no sería posible que un usuario cancelara la solicitud de configuración de llamada en curso hasta que se haya completado la marcación y se hayan enviado todos los dígitos al conmutador.

-   Las funciones que devuelven información (como [**lineGetCallInfo)**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)devuelven SUCCESS solo cuando la información solicitada está disponible para la aplicación. Las funciones que devuelven identificadores (a líneas o llamadas) solo pueden devolver SUCCESS después de que el identificador sea válido. No se debe enviar ningún mensaje sobre esa línea o llamada antes de la indicación SUCCESS de la función que provocó su creación. El proveedor de servicios es responsable de suprimir estos mensajes.
-   Las funciones que habilitan ciertas condiciones permanentes (como [**lineMonitorDigits)**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)devuelven SUCCESS solo después de habilitar la condición, no cuando la condición se quita de nuevo (por ejemplo, no cuando se ha completado toda la supervisión de dígitos).
-   Las funciones de control de llamadas (como [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold) o [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), pero no [**lineMakeCall)**](/windows/win32/api/tapi/nf-tapi-linemakecall)devuelven SUCCESS cuando se completa la operación. Algunas redes telefónicas no proporcionan confirmación (positiva o negativa) sobre la finalización de determinadas solicitudes realizadas por proveedores de servicios. En tales situaciones, el proveedor de servicios debe decidir si la solicitud se ha hecho correcta o no. Por lo tanto, SUCCESS puede indicar que el proveedor de servicios ha iniciado acciones para satisfacer la solicitud, pero no necesariamente nada más. Por ejemplo, es posible que el proveedor no reciba ninguna confirmación afirmativa a su solicitud del modificador, aunque ya ha enviado un mensaje de confirmación correcta a la aplicación.

## <a name="tapi-3x"></a>TAPI 3.x

Cuando una operación devuelve una indicación SUCCESS (ya sea sincrónicamente cuando la función devuelve para las operaciones sincrónicas o de forma asincrónica con una llamada al procedimiento de devolución de llamada [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) para las operaciones asincrónicas), se supone que lo siguiente es true:

-   La función ha progresado correctamente hasta un punto definido por el proveedor de servicios. El proveedor de servicios define el punto en función de función por función. Después de llegar a ese punto, la operación ha finalizado completamente o se encuentra en un estado tal que los mensajes de estado independientes posteriores informarán a la aplicación sobre el progreso.
-   Las funciones que devuelven información (como [**TSPI \_ linePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) o [**TSPI \_ lineDevSpecific)**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)devuelven SUCCESS solo cuando la información solicitada está disponible para el autor de la llamada. Las funciones que devuelven identificadores (a líneas abiertas, teléfonos abiertos o llamadas) devuelven los identificadores inmediatamente en la devolución de la función. Tanto el proveedor de servicios como el autor de la llamada deben tratar los identificadores como "aún no válidos" hasta la indicación success final. El proveedor de servicios es responsable de evitar cualquier mensaje de devolución de llamada al procedimiento [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) o [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) sobre esa línea abierta, teléfono abierto o llamada hasta después de la indicación SUCCESS. Si el resultado final es un error, cualquier identificador devuelto inmediatamente deja de ser válido sin ninguna acción adicional.
-   Las funciones que habilitan ciertas condiciones permanentes (como [**TSPI \_ lineMonitorDigits)**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)devuelven SUCCESS solo después de habilitar la condición, no cuando la condición se quita de nuevo (por ejemplo, no cuando se completa la supervisión de dígitos).
-   Las funciones de control de llamadas (como [**TSPI \_ lineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) y [**TSPI \_ lineSetupTransfer,**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)pero no [**TSPI \_ lineMakeCall)**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)devuelven SUCCESS cuando se completa la operación. En entornos de telefonía que no proporcionan una confirmación positiva de estas funciones, el proveedor de servicios se ve obligado a tomar la mejor decisión sobre el éxito o el error de la función.
-   La implementación de un proveedor de servicios de [**la línea \_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) debe devolver SUCCESS a más tardar cuando la llamada entra en el *estado de llamada* siguiente. Lo ideal es que el proveedor indique SUCCESS lo antes posible, como cuando la llamada entra en el estado de llamada *de dialtone* (si procede). Cuando se devuelve SUCCESS a la aplicación, los mensajes [**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) informan al autor de la llamada sobre el progreso de la llamada. Los proveedores de servicios que retrasan la devolución de la indicación **TSPI \_ lineMakeCall** SUCCESS, por ejemplo, hasta que se completa la marcación, limitan gravemente la flexibilidad en el nivel de aplicación. El retraso en la devolución de SUCCESS en la línea **\_ TSPIMakeCall** impide que un usuario cancele la solicitud de configuración de llamada en curso hasta que se complete la marcación y todos los dígitos se envíen al conmutador.

 

 
