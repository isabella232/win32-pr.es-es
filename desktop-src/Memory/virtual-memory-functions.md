---
description: Las funciones de memoria virtual permiten a un proceso manipular o determinar el estado de las páginas en su espacio de direcciones virtuales.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Funciones de memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee6839a00c573a3724cd22b3d304fef4276db29507c89802b42602120180bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105715"
---
# <a name="virtual-memory-functions"></a>Funciones de memoria virtual

Las funciones de memoria virtual permiten a un proceso manipular o determinar el estado de las páginas en su espacio de direcciones virtuales. Pueden realizar las siguientes operaciones:

-   Reserve un intervalo de espacio de direcciones virtuales de un proceso. Reservar espacio de direcciones no asigna ningún almacenamiento físico, pero impide que otras operaciones de asignación utilicen el intervalo especificado. No afecta a los espacios de direcciones virtuales de otros procesos. Reservar páginas evita el consumo necesario de almacenamiento físico, al tiempo que permite que un proceso reserve un intervalo de su espacio de direcciones en el que puede crecer una estructura de datos dinámica. El proceso puede asignar almacenamiento físico para este espacio, según sea necesario.
-   Confirme un intervalo de páginas reservadas en el espacio de direcciones virtuales de un proceso para que el almacenamiento físico (ya sea en RAM o en disco) solo sea accesible para el proceso de asignación.
-   Especifique lectura/escritura, solo lectura o sin acceso para un intervalo de páginas confirmadas. Esto difiere de las funciones de asignación estándar que siempre asignan páginas con acceso de lectura y escritura.
-   Liberar un intervalo de páginas reservadas, lo que hace que el intervalo de direcciones virtuales esté disponible para las operaciones de asignación posteriores por el proceso de llamada.
-   Desacomprima una serie de páginas confirmadas, liberando su almacenamiento físico y haciendo que esté disponible para su posterior asignación por cualquier proceso.
-   Bloquee una o varias páginas de memoria confirmada en la memoria física (RAM) para que el sistema no pueda intercambiar las páginas al archivo de paginación.
-   Obtenga información sobre un intervalo de páginas en el espacio de direcciones virtuales del proceso de llamada o de un proceso especificado.
-   Cambie la protección de acceso para un intervalo especificado de páginas confirmadas en el espacio de direcciones virtuales del proceso de llamada o de un proceso especificado.

Para obtener más información, vea los temas siguientes:

-   [Asignación de memoria virtual](allocating-virtual-memory.md)
-   [Comparar métodos de asignación de memoria](comparing-memory-allocation-methods.md)
-   [Liberar memoria virtual](freeing-virtual-memory.md)
-   [Trabajar con páginas](working-with-pages.md)
-   [Funciones de administración de memoria](memory-management-functions.md)

 

 



