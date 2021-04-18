---
description: Para determinar el tamaño de una página en el equipo actual, utilice la función GetSystemInfo.
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: Trabajar con páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c12c99ada03dca1e17c72c2a5f0d5360b6a98d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543043"
---
# <a name="working-with-pages"></a>Trabajar con páginas

Para determinar el tamaño de una página en el equipo actual, utilice la función [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Las funciones [**VirtualQuery (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) y [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) devuelven información sobre una región de páginas consecutivas que empiezan en una dirección especificada en el espacio de direcciones de un proceso. **VirtualQuery (** devuelve información sobre la memoria en el proceso de llamada. **VirtualQueryEx** devuelve información sobre la memoria en un proceso especificado y se usa para admitir depuradores que necesitan información sobre un proceso que se está depurando. La región de las páginas está limitada por la dirección especificada hacia abajo hasta el límite de la página más cercana. Extiende a través de todas las páginas siguientes con los siguientes atributos en común:

-   El estado de todas las páginas es el mismo: confirmado, reservado o libre.
-   Si la página inicial no es gratuita, todas las páginas de la región forman parte de la misma asignación inicial de páginas reservadas por una llamada a [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   La protección de acceso de todas las páginas es la misma (es decir, la página **\_ solo lectura**, la **página \_ ReadWrite** o el **\_ acceso a páginas**).

La función [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) permite que un proceso bloquee una o varias páginas de la memoria asignada en la memoria física (RAM), evitando que el sistema intercambie las páginas en el archivo de paginación. Se puede usar para asegurarse de que se pueda acceder a los datos críticos sin tener acceso al disco. Bloquear las páginas en la memoria es peligroso porque restringe la capacidad del sistema para administrar la memoria. El uso excesivo de **VirtualLock** puede reducir el rendimiento del sistema, ya que hace que el código ejecutable se intercambie en el archivo de paginación. La función [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) desbloquea la memoria bloqueada por **VirtualLock**.

La función [**VirtualProtect (**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) permite a un proceso modificar la protección de acceso de cualquier página confirmada en el espacio de direcciones de un proceso. Por ejemplo, un proceso puede asignar páginas de lectura/escritura para almacenar datos confidenciales y, a continuación, puede cambiar el acceso a solo lectura o no tener acceso a la protección contra sobrescritura accidental. **VirtualProtect (** se utiliza normalmente con páginas asignadas por [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), pero también funciona con páginas confirmadas por cualquiera de las demás funciones de asignación. Sin embargo, **VirtualProtect (** cambia la protección de todas las páginas y los punteros devueltos por las demás funciones no se alinean necesariamente en los límites de la página. La función [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) es similar a **VirtualProtect (**, salvo que cambia la protección de la memoria en un proceso especificado. Cambiar la protección resulta útil para los depuradores en el acceso a la memoria de un proceso que se está depurando.

 

 
