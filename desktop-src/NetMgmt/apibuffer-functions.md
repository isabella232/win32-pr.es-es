---
title: Funciones de ApiBuffer
description: Las funciones apiBuffer de administración de red se usan para administrar la asignación de memoria que usa una aplicación con funciones de administración de red.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169366"
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



 

Para las funciones remotables que devuelven información al autor de la llamada, la biblioteca en tiempo de ejecución rpc asigna el búfer que contiene la información de devolución. Cuando el autor de la llamada haya terminado de procesar la información, debe llamar a la [**función NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) para liberar el búfer asignado.

 

 