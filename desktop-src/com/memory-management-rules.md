---
title: Reglas de administración de memoria
description: Reglas de administración de memoria
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6cd7070a6a353994cba556bd967c6f7805cdb094504b87a87a96bb6de138c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918564"
---
# <a name="memory-management-rules"></a>Reglas de administración de memoria

La duración de los punteros a interfaces siempre se administra a través de los [**métodos AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) [**y Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en cada interfaz COM. Para obtener más información, vea [Reglas para administrar recuentos de referencias.](rules-for-managing-reference-counts.md)

Para todos los demás parámetros, es importante cumplir ciertas reglas para administrar la memoria. Las reglas siguientes se aplican a todos los parámetros de los métodos de interfaz, incluido el valor devuelto, que no se pasan por valor:

-   El autor de la llamada debe asignar y liberar los parámetros en .
-   El parámetro out-parameters debe asignarse mediante el llamado; El autor de la llamada las libera mediante el asignador de memoria de tareas COM estándar. Vea [El asignador de memoria OLE](the-ole-memory-allocator.md) para obtener más información.
-   In/out-parameters are initially allocated by the caller, and then freed and reallocated by the one called, if necessary. Como sucede con los parámetros out, el autor de la llamada es responsable de liberar el valor devuelto final. Se debe usar el asignador de memoria COM estándar.

En los dos últimos casos, donde un fragmento de código asigna la memoria y otro fragmento de código la libera, el uso del asignador COM garantiza que los dos fragmentos de código usan los mismos métodos de asignación.

Otra área que necesita atención especial es el tratamiento de los parámetros fuera y fuera en condiciones de error. Si una función devuelve un código de error, el autor de la llamada normalmente no tiene ninguna manera de limpiar los parámetros out o in-out. Esto conduce a las siguientes reglas adicionales:

-   En caso de una condición de error, los parámetros siempre deben establecerse de forma confiable en un valor que se limpiará sin que el autor de la llamada haga nada.
-   Todos los parámetros de puntero de salida deben establecerse explícitamente en **NULL.** Normalmente se pasan en un parámetro de puntero a puntero, pero también se pueden pasar como miembros de una estructura que el autor de la llamada asigna y el código llamado se rellena. La manera más sencilla de asegurarse de que esto es (en parte) para establecer estos valores en **NULL en** la entrada de función. Esta regla es importante porque promueve una interoperabilidad de aplicaciones más sólida.
-   En condiciones de error, todos los parámetros de entrada y salida se deben dejar solos por el código llamado (por lo tanto, permanecer en el valor en el que el autor de la llamada los inicializó) o establecerse explícitamente, como en el caso de devolución de error de parámetro out.

Recuerde que estas convenciones de administración de memoria para aplicaciones COM solo se aplican a través de interfaces públicas y API. No es necesario que la asignación de memoria estrictamente interna a una aplicación COM se haga mediante estos mecanismos.

COM usa internamente llamadas a procedimiento remoto (RPC) para comunicarse entre clientes y servidores. Para obtener más información sobre la administración de memoria en código auxiliar del servidor RPC, vea el tema [Administración de memoria de código auxiliar del](../rpc/server-stub-memory-management.md) servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de la asignación de memoria](managing-memory-allocation.md)
</dt> </dl>

 

 