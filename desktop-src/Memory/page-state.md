---
description: Las páginas del espacio de direcciones virtuales de un proceso pueden estar en uno de los Estados siguientes.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Estado de la página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a1e5d3170197cf977f0b1a91898ee150086ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279485"
---
# <a name="page-state"></a>Estado de la página

Las páginas del espacio de direcciones virtuales de un proceso pueden estar en uno de los Estados siguientes.



| Estado     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuito      | La página no se confirma ni se reserva. La página no es accesible para el proceso. Está disponible para reservarse, confirmarse o reservarse y confirmarse simultáneamente. Al intentar leer o escribir en una página libre, se produce una excepción de infracción de acceso. <br/> Un proceso puede utilizar la función [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para liberar las páginas reservadas o confirmadas de su espacio de direcciones y devolverlas al estado Free.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reservado  | La página se ha reservado para uso futuro. Otras funciones de asignación no pueden usar el intervalo de direcciones. No se puede tener acceso a la página y no tiene ningún almacenamiento físico asociado. Está disponible para su confirmación. <br/> Un proceso puede usar la función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para reservar páginas de su espacio de direcciones y más adelante para confirmar las páginas reservadas. Puede usar [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para anular la confirmación de las páginas confirmadas y devolverlas al estado reservado.<br/>                                                                                                                                                                                                                          |
| Confirmado | Se han asignado cargos de memoria del tamaño total de la RAM y de los archivos de paginación en el disco. La página es accesible y el acceso se controla mediante una de las [constantes de protección de memoria](memory-protection-constants.md). El sistema inicializa y carga cada página confirmada en la memoria física solo durante el primer intento de leer o escribir en esa página. Cuando finaliza el proceso, el sistema libera el almacenamiento de las páginas confirmadas. <br/> Un proceso puede usar [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para confirmar páginas físicas desde una región reservada. También pueden reservar y confirmar páginas simultáneamente.<br/> Las funciones [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) asignan páginas confirmadas con acceso de lectura y escritura.<br/> |



 

 

 
