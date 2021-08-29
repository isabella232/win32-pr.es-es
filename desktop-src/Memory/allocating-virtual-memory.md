---
description: Las funciones de memoria virtual manipulan páginas de memoria. Las funciones usan el tamaño de una página en el equipo actual para redondear los tamaños y direcciones especificados.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Asignación de memoria virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77039db22d4a9d2897e1269e3ee82902c81fae2274bea12d5a7f7abbaa9e7d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963475"
---
# <a name="allocating-virtual-memory"></a>Asignación de memoria virtual

Las funciones de memoria virtual manipulan páginas de memoria. Las funciones usan el tamaño de una página en el equipo actual para redondear los tamaños y direcciones especificados.

La [**función VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) realiza una de las siguientes operaciones:

-   Reserva una o varias páginas gratuitas.
-   Confirma una o varias páginas reservadas.
-   Reserva y confirma una o varias páginas gratuitas.

Puede especificar la dirección inicial de las páginas que se reservarán o se confirman, o bien puede permitir que el sistema determine la dirección. La función redondea la dirección especificada al límite de página adecuado. Las páginas reservadas no son accesibles, pero las páginas asignadas se pueden asignar con el acceso **PAGE \_ READWRITE,** **PAGE \_ READONLY** o **PAGE \_ NOACCESS.** Cuando se confirman las páginas, los cargos de memoria se asignan a partir del tamaño total de la RAM y los archivos de paginación en el disco, pero cada página se inicializa y carga en la memoria física solo en el primer intento de lectura o escritura en esa página. Puede usar referencias de puntero normales para acceder a la memoria que confirma [**la función VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

 

 
