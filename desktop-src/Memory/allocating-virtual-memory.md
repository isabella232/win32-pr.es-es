---
description: Las funciones de memoria virtual manipulan páginas de memoria. Las funciones usan el tamaño de una página en el equipo actual para redondear los tamaños y direcciones especificados.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Asignación de memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360673"
---
# <a name="allocating-virtual-memory"></a>Asignación de memoria virtual

Las funciones de memoria virtual manipulan páginas de memoria. Las funciones usan el tamaño de una página en el equipo actual para redondear los tamaños y direcciones especificados.

La función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) realiza una de las operaciones siguientes:

-   Reserva una o más páginas libres.
-   Confirma una o más páginas reservadas.
-   Reserva y confirma una o varias páginas libres.

Puede especificar la dirección de inicio de las páginas que se van a reservar o confirmar, o puede permitir que el sistema determine la dirección. La función redondea la dirección especificada al límite de página adecuado. No se puede acceder a las páginas reservadas, pero las páginas confirmadas se pueden asignar con el acceso **Page \_ ReadWrite**, **Page \_ ReadOnly** o **Page \_ NoAccess** . Cuando se confirman páginas, se asignan cargos de memoria desde el tamaño total de la RAM y los archivos de paginación en el disco, pero cada página se inicializa y se carga en la memoria física solo en el primer intento de leer o escribir en esa página. Puede utilizar referencias de puntero normales para tener acceso a la memoria confirmada por la función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .

 

 
