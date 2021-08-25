---
title: Funciones de ApiBuffer
description: Las funciones apiBuffer de administración de red se usan para administrar la asignación de memoria que usa una aplicación con funciones de administración de red.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0778c216860fe16a673e1bdcc2ac470cbb52a128f0e08d4d32d98df929bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912485"
---
# <a name="apibuffer-functions"></a>Funciones de ApiBuffer

Las funciones apiBuffer de administración de red se usan para administrar la asignación de memoria que usa una aplicación con funciones de administración de red. Sin embargo, en general, para otra memoria usada por una aplicación, debe usar las funciones de administración de memoria [en](/windows/desktop/Memory/memory-management-functions) lugar de estas funciones apiBuffer.

Las funciones apiBuffer se enumeran a continuación.



| Función                                                 | Descripción                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Asigna memoria del montón. Llame a esta función cuando necesite compatibilidad con la **función NetApiBufferFree.** |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera la memoria asignada por la función **NetApiBufferAllocate** y otras funciones de administración de red.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Cambia el tamaño de un búfer asignado por una llamada a la **función NetApiBufferAllocate.**                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Devuelve el tamaño, en bytes, de un búfer asignado por una llamada a la **función NetApiBufferAllocate.**                     |



 

En el caso de las funciones remotables que devuelven información al autor de la llamada, la biblioteca rpc en tiempo de ejecución asigna el búfer que contiene la información de devolución. Cuando el autor de la llamada haya terminado de procesar la información, debe llamar a la [**función NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar el búfer asignado.

 

 