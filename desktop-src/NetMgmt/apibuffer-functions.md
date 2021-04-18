---
title: Funciones de ApiBuffer
description: Las funciones de ApiBuffer de administración de red se usan para administrar la asignación de memoria utilizada por una aplicación con funciones de administración de red.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665848"
---
# <a name="apibuffer-functions"></a>Funciones de ApiBuffer

Las funciones de ApiBuffer de administración de red se usan para administrar la asignación de memoria utilizada por una aplicación con funciones de administración de red. Sin embargo, en general, para otra memoria utilizada por una aplicación, debe usar las [funciones de administración de memoria](/windows/desktop/Memory/memory-management-functions) en lugar de estas funciones ApiBuffer.

A continuación se enumeran las funciones de ApiBuffer.



| Función                                                 | Descripción                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Asigna memoria del montón. Llame a esta función cuando necesite compatibilidad con la función **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera memoria asignada por la función **NetApiBufferAllocate** y otras funciones de administración de redes.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Cambia el tamaño de un búfer asignado por una llamada a la función **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Devuelve el tamaño, en bytes, de un búfer asignado por una llamada a la función **NetApiBufferAllocate** .                     |



 

En el caso de las funciones de uso remoto que devuelven información al llamador, la biblioteca en tiempo de ejecución de RPC asigna el búfer que contiene la información de devolución. Cuando el autor de la llamada ha terminado de procesar la información, debe llamar a la función [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar el búfer asignado.

 

 