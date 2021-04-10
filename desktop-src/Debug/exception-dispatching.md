---
description: Cuando se produce una excepción de hardware o software, el procesador detiene la ejecución en el punto en el que se produjo la excepción y transfiere el control al sistema.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Envío de excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02b40aa132541fe88d692cbbf1881a8b620a209
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152733"
---
# <a name="exception-dispatching"></a>Envío de excepciones

Cuando se produce una excepción de hardware o software, el procesador detiene la ejecución en el punto en el que se produjo la excepción y transfiere el control al sistema. En primer lugar, el sistema guarda el estado de la máquina del subproceso actual y la información que describe la excepción. Después, el sistema intenta encontrar un controlador de excepciones para controlar la excepción.

El estado de la máquina del subproceso en el que se produjo la excepción se guarda en una estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) . Esta información (denominada *registro de contexto*) permite al sistema continuar la ejecución en el punto de la excepción si la excepción se controla correctamente. La descripción de la excepción (denominada **registro de excepción**) se guarda en una estructura de [**\_ registro de excepciones**](/windows/desktop/api/WinNT/ns-winnt-exception_record) . Dado que almacena la información dependiente del equipo del registro de contexto por separado de la información independiente del equipo del registro de excepción, el mecanismo de control de excepciones es portable a distintas plataformas.

La información en los registros de contexto y de excepción está disponible por medio de la función [**GetExceptionInformation**](getexceptioninformation.md) y puede ponerse a disposición de los controladores de excepciones que se ejecuten como resultado de la excepción. El registro de excepciones incluye la siguiente información.

-   Código de excepción que identifica el tipo de excepción.
-   Marcas que indican si la excepción es continuable. Cualquier intento de continuar la ejecución después de una excepción no continuada genera otra excepción.
-   Puntero a otro registro de excepción. Esto facilita la creación de una lista vinculada de excepciones si se producen excepciones anidadas.
-   Dirección en la que se produjo la excepción.
-   Matriz de argumentos que proporcionan información adicional sobre la excepción.

Cuando se produce una excepción en el código de modo de usuario, el sistema utiliza el siguiente orden de búsqueda para encontrar un controlador de excepciones:

1.  Si se está depurando el proceso, el sistema lo notifica al depurador. Para obtener más información, vea [control de excepciones del depurador](debugger-exception-handling.md).
2.  Si no se está depurando el proceso, o si el depurador asociado no controla la excepción, el sistema intenta encontrar un controlador de excepciones basado en marco buscando en los marcos de pila del subproceso en el que se produjo la excepción. El sistema busca primero en el marco de pila actual y, a continuación, busca en los marcos de pila anteriores en orden inverso.
3.  Si no se puede encontrar ningún controlador basado en fotogramas, o si ningún controlador basado en marco controla la excepción, pero el proceso se está depurando, el sistema notifica al depurador por segunda vez.
4.  Si no se está depurando el proceso, o si el depurador asociado no controla la excepción, el sistema proporciona el control predeterminado basado en el tipo de excepción. Para la mayoría de las excepciones, la acción predeterminada es llamar a la función [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .

Cuando se produce una excepción en el código en modo kernel, el sistema busca en los marcos de pila de la pila de kernel en un intento de buscar un controlador de excepciones. Si no se encuentra un controlador o ningún controlador controla la excepción, el sistema se apaga como si se hubiera llamado a la función [**ExitWindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) .

 

 
