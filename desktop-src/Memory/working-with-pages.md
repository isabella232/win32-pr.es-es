---
description: Para determinar el tamaño de una página en el equipo actual, use la función GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Trabajar con Pages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c12c99ada03dca1e17c72c2a5f0d5360b6a98d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159789"
---
# <a name="working-with-pages"></a>Trabajar con Pages

Para determinar el tamaño de una página en el equipo actual, use la [**función GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

Las [**funciones VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) y [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) devuelven información sobre una región de páginas consecutivas que comienza en una dirección especificada en el espacio de direcciones de un proceso. **VirtualQuery** devuelve información sobre la memoria en el proceso de llamada. **VirtualQueryEx devuelve** información sobre la memoria en un proceso especificado y se usa para admitir depuradores que necesitan información sobre un proceso que se está depurando. La región de páginas está limitada por la dirección especificada redondeada hacia abajo hasta el límite de página más cercano. Se extiende a través de todas las páginas posteriores con los siguientes atributos en común:

-   El estado de todas las páginas es el mismo: confirmado, reservado o gratuito.
-   Si la página inicial no es gratuita, todas las páginas de la región forman parte de la misma asignación inicial de páginas reservadas por una llamada a [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   La protección de acceso de todas las páginas es la misma (es decir, **PAGE \_ READONLY,** **PAGE \_ READWRITE** o **PAGE \_ NOACCESS).**

La [**función VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) permite que un proceso bloquee una o varias páginas de memoria confirmada en memoria física (RAM), lo que impide que el sistema intercambie las páginas al archivo de paginación. Se puede usar para asegurarse de que los datos críticos son accesibles sin acceso al disco. Bloquear páginas en la memoria es peligroso porque restringe la capacidad del sistema para administrar la memoria. El uso excesivo **de VirtualLock** puede degradar el rendimiento del sistema al hacer que el código ejecutable se intercambie al archivo de paginación. La [**función VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) desbloquea la memoria bloqueada por **VirtualLock.**

La [**función VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) permite a un proceso modificar la protección de acceso de cualquier página confirmada en el espacio de direcciones de un proceso. Por ejemplo, un proceso puede asignar páginas de lectura y escritura para almacenar datos confidenciales y, a continuación, puede cambiar el acceso a solo lectura o a ningún acceso para proteger contra la sobrescritura accidental. **VirtualProtect** se usa normalmente con páginas asignadas por [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), pero también funciona con páginas que confirma cualquiera de las otras funciones de asignación. Sin embargo, **VirtualProtect** cambia la protección de páginas enteras y los punteros devueltos por las demás funciones no se alinean necesariamente en los límites de página. La [**función VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) es similar a **VirtualProtect,** salvo que cambia la protección de la memoria en un proceso especificado. Cambiar la protección es útil para los depuradores a la hora de acceder a la memoria de un proceso que se está depurando.

 

 
