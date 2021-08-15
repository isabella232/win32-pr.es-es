---
description: Las páginas del espacio de direcciones virtuales de un proceso pueden estar en uno de los siguientes estados.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Estado de página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ec9c162220cd0c1accdb35e35309082a2e94c4af6023af7e7d9d7cd55be620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386408"
---
# <a name="page-state"></a>Estado de página

Las páginas del espacio de direcciones virtuales de un proceso pueden estar en uno de los siguientes estados.



| Estado     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuito      | La página no está ni confirmada ni reservada. La página no es accesible para el proceso. Está disponible para estar reservado, confirmado o reservado y confirmado simultáneamente. Al intentar leer o escribir en una página gratuita, se produce una excepción de infracción de acceso. <br/> Un proceso puede usar las funciones [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para liberar páginas reservadas o confirmadas de su espacio de direcciones, devolviendolas al estado libre.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reservada  | La página se ha reservado para su uso futuro. Otras funciones de asignación no pueden usar el intervalo de direcciones. La página no es accesible y no tiene ningún almacenamiento físico asociado. Está disponible para su confirmación. <br/> Un proceso puede usar las [**funciones VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para reservar páginas de su espacio de direcciones y, posteriormente, confirmar las páginas reservadas. Puede usar [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx para**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) desajustar las páginas confirmadas y devolverlas al estado reservado.<br/>                                                                                                                                                                                                                          |
| Confirmado | Los cargos de memoria se han asignado a partir del tamaño total de la RAM y los archivos de paginación en el disco. La página es accesible y el acceso se controla mediante una de las constantes [de protección de memoria](memory-protection-constants.md). El sistema inicializa y carga cada página confirmada en la memoria física solo durante el primer intento de lectura o escritura en esa página. Cuando finaliza el proceso, el sistema libera el almacenamiento para las páginas confirmadas. <br/> Un proceso puede usar [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para confirmar páginas físicas de una región reservada. También pueden reservar y confirmar páginas simultáneamente.<br/> Las [**funciones GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) asignan páginas asignadas con acceso de lectura/escritura.<br/> |



 

 

 
