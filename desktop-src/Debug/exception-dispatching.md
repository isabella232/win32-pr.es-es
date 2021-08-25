---
description: Cuando se produce una excepción de hardware o software, el procesador detiene la ejecución en el punto en el que se produjo la excepción y transfiere el control al sistema.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Distribución de excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b7b4f73c9d2c3fbaf15b4390ee6ecc6b9aa06b50524ec080fc45319d3b94767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912735"
---
# <a name="exception-dispatching"></a>Distribución de excepciones

Cuando se produce una excepción de hardware o software, el procesador detiene la ejecución en el punto en el que se produjo la excepción y transfiere el control al sistema. En primer lugar, el sistema guarda el estado de la máquina del subproceso actual y la información que describe la excepción. A continuación, el sistema intenta encontrar un controlador de excepciones para controlar la excepción.

El estado de la máquina del subproceso en el que se produjo la excepción se guarda en una [**estructura CONTEXT.**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Esta información (denominada registro *de contexto)* permite al sistema continuar la ejecución en el punto de la excepción si la excepción se controla correctamente. La descripción de la excepción (denominada registro **de excepción)** se guarda en una [**estructura EXCEPTION \_ RECORD.**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Dado que almacena la información dependiente de la máquina del registro de contexto por separado de la información independiente del equipo del registro de excepciones, el mecanismo de control de excepciones se puede transportar a distintas plataformas.

La información de los registros de contexto y de excepción está disponible mediante la función [**GetExceptionInformation**](getexceptioninformation.md) y puede estar disponible para cualquier controlador de excepciones que se ejecute como resultado de la excepción. El registro de excepción incluye la siguiente información.

-   Código de excepción que identifica el tipo de excepción.
-   Marcas que indican si la excepción es continuable. Cualquier intento de continuar la ejecución después de una excepción no pertinente genera otra excepción.
-   Puntero a otro registro de excepción. Esto facilita la creación de una lista vinculada de excepciones si se producen excepciones anidadas.
-   Dirección en la que se produjo la excepción.
-   Matriz de argumentos que proporcionan información adicional sobre la excepción.

Cuando se produce una excepción en el código de modo de usuario, el sistema usa el siguiente orden de búsqueda para buscar un controlador de excepciones:

1.  Si el proceso se está depurando, el sistema notifica al depurador. Para obtener más información, vea [Control de excepciones del depurador.](debugger-exception-handling.md)
2.  Si el proceso no se depura o si el depurador asociado no controla la excepción, el sistema intenta buscar un controlador de excepciones basado en fotogramas buscando los marcos de pila del subproceso en el que se produjo la excepción. El sistema busca primero en el marco de pila actual y, a continuación, busca en los marcos de pila anteriores en orden inverso.
3.  Si no se encuentra ningún controlador basado en fotogramas o ningún controlador basado en fotogramas controla la excepción, pero el proceso se está depurando, el sistema notifica al depurador una segunda vez.
4.  Si el proceso no se depura o si el depurador asociado no controla la excepción, el sistema proporciona un control predeterminado basado en el tipo de excepción. Para la mayoría de las excepciones, la acción predeterminada es llamar a la [**función ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)

Cuando se produce una excepción en el código en modo kernel, el sistema busca en los marcos de pila de la pila del kernel en un intento de encontrar un controlador de excepciones. Si no se encuentra un controlador o ningún controlador controla la excepción, el sistema se cierra como si se hubiera llamado a la función [**ExitWindows.**](/windows/win32/api/winuser/nf-winuser-exitwindows)

 

 
