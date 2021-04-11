---
title: Reglas de administración de memoria
description: Reglas de administración de memoria
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149673"
---
# <a name="memory-management-rules"></a>Reglas de administración de memoria

La duración de los punteros a las interfaces siempre se administra a través de los métodos [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en cada interfaz com. Para obtener más información, vea [rules for Managing Reference Counts](rules-for-managing-reference-counts.md).

En el caso de todos los demás parámetros, es importante cumplir ciertas reglas para administrar la memoria. Las siguientes reglas se aplican a todos los parámetros de la interfaz methodsâ ", incluido el valor devuelto valueâ €" que no se pasan por valor:

-   El autor de la llamada debe asignar y liberar los parámetros in-.
-   Out-Parameters debe ser asignado por el llamado; los libera el autor de la llamada mediante el asignador de memoria de tareas COM estándar. Para obtener más información, vea [asignador de memoria OLE](the-ole-memory-allocator.md) .
-   Los parámetros in/out-se asignan inicialmente mediante el autor de la llamada y, a continuación, se liberan y reasignan mediante el llamado, si es necesario. Como sucede con los parámetros out, el llamador es responsable de liberar el valor devuelto final. Se debe utilizar el asignador de memoria COM estándar.

En los dos últimos casos, en los que un fragmento de código asigna la memoria y otro fragmento de código la libera, el asignador COM garantiza que los dos fragmentos de código usen los mismos métodos de asignación.

Otra área que necesita atención especial es el tratamiento de los parámetros out y out en las condiciones de error. Si una función devuelve un código de error, el llamador normalmente no tiene ninguna manera de limpiar los parámetros out o out. Esto conduce a las siguientes reglas adicionales:

-   En el caso de una condición de error, los parámetros siempre se deben establecer de forma confiable en un valor que se limpie sin ninguna acción por parte del llamador.
-   Todos los parámetros de puntero se deben establecer explícitamente en **null**. Normalmente se pasan en un parámetro de puntero a puntero, pero también se pueden pasar como miembros de una estructura que el autor de la llamada asigna y se rellena el código llamado. La manera más sencilla de asegurarse de esto es (en parte) establecer estos valores en **null** en la entrada de la función. Esta regla es importante porque promueve una interoperabilidad de aplicaciones más sólida.
-   En condiciones de error, todos los parámetros de salida deben dejarse solo por el código llamado (que permanece en el valor al que el llamador ha inicializado) o establecerse explícitamente, como en el caso de devolución de error del parámetro out.

Recuerde que estas convenciones de administración de memoria para las aplicaciones COM se aplican solo a través de las interfaces públicas y APIsâ "no hay ningún requisito en todo lo que la asignación de memoria es estrictamente interna para una aplicación COM debe realizarse mediante estos mecanismos.

COM utiliza internamente llamadas a procedimiento remoto (RPC) para comunicarse entre clientes y servidores. Para obtener más información acerca de la administración de memoria en códigos auxiliares de servidor RPC, consulte el tema [Server-stub Memory Management](../rpc/server-stub-memory-management.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar la asignación de memoria](managing-memory-allocation.md)
</dt> </dl>

 

 