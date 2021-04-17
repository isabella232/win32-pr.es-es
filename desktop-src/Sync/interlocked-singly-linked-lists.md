---
description: Una lista de vinculación única (SList) entrelazada facilita la tarea de inserción y eliminación de una lista vinculada.
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: Listas vinculadas de un solo vínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af39847fa2fd1b1873c661d6ec904783e0139b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667978"
---
# <a name="interlocked-singly-linked-lists"></a>Listas vinculadas de un solo vínculo

Una *lista de vinculación única* (SList) entrelazada facilita la tarea de inserción y eliminación de una lista vinculada. Los SLists se implementan mediante un algoritmo de no bloqueo para proporcionar sincronización atómica, aumentar el rendimiento del sistema y evitar problemas como los convoyes de inversion prioritarios y de bloqueo.

SLists son fáciles de implementar y usar en el código de 32 bits. Sin embargo, es desafiante implementarlas en código de 64 bits, porque la cantidad de datos que se intercambian con las primitivas de intercambio de interbloqueos nativas no es el doble del tamaño de la dirección, como en el código de 32 bits. Por lo tanto, SLists permiten migrar algoritmos escalables de alto nivel a Windows.

**Windows 8:** A partir de Windows 8, las primitivas de intercambio nativas de interbloqueos adecuadas están disponibles para el código de 64 bits, por ejemplo [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)).

Las aplicaciones pueden utilizar SLists mediante una llamada a la función [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) para inicializar el encabezado de la lista. Para insertar elementos en la lista, utilice la función [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) . Para eliminar elementos de la lista, utilice la función [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) .

Todos los elementos de lista se deben alinear en un límite de **\_ \_ alineación de asignación de memoria** . Los elementos no alineados pueden producir resultados imprevisibles. Vea **\_ \_ malloc alineado**.

Para ver un ejemplo, consulte [uso de listas vinculadas](using-singly-linked-lists.md)de una sola vez.

En la tabla siguiente se enumeran las funciones SList.



| Función                                                         | Descripción                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | Inicializa el encabezado de una lista vinculada individualmente.                                                                                                             |
| [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | Vacía la lista completa de elementos de una lista vinculada de una sola vez.                                                                                                 |
| [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | Quita un elemento de la parte delantera de una lista vinculada individualmente.                                                                                                   |
| [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | Inserta un elemento al principio de una lista vinculada individualmente.                                                                                                     |
| [**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))     | Inserta una lista vinculada individualmente en la parte frontal de otra lista vinculada de forma individual.                                                                                  |
| [**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | Inserta una lista vinculada individualmente en la parte frontal de otra lista vinculada de forma individual. Esta versión del método no usa la Convención de llamada **\_ \_ fastcall** . |
| [**RtlFirstEntrySList**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | Recupera la primera entrada de una lista vinculada individualmente.                                                                                                        |
| [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | Recupera el número de entradas de la lista de vínculos de entrada especificada.                                                                                      |



 

 

 
