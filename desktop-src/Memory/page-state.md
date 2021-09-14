---
description: Las páginas del espacio de direcciones virtuales de un proceso pueden estar en uno de los estados siguientes.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Estado de la página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a1e5d3170197cf977f0b1a91898ee150086ddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159821"
---
# <a name="page-state"></a>Estado de la página

Las páginas del espacio de direcciones virtuales de un proceso pueden estar en uno de los estados siguientes.



| State     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuito      | La página no se confirma ni se reserva. El proceso no puede acceder a la página. Está disponible para reservarse, confirmado o reservado y confirmado simultáneamente. Al intentar leer o escribir en una página gratuita, se produce una excepción de infracción de acceso. <br/> Un proceso puede usar la [**función VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) para liberar páginas reservadas o confirmadas de su espacio de direcciones, devolviendolas al estado libre.<br/>                                                                                                                                                                                                                                                                                                                              |
| Reservada  | La página se ha reservado para su uso futuro. Otras funciones de asignación no pueden usar el intervalo de direcciones. La página no es accesible y no tiene ningún almacenamiento físico asociado. Está disponible para ser confirmado. <br/> Un proceso puede usar la [**función VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para reservar páginas de su espacio de direcciones y versiones posteriores para confirmar las páginas reservadas. Puede usar [**VirtualFree o**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) [**VirtualFreeEx para**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) desajustar las páginas confirmadas y devolverlas al estado reservado.<br/>                                                                                                                                                                                                                          |
| Confirmado | Los cargos de memoria se han asignado a partir del tamaño total de la RAM y de los archivos de paginación en disco. La página es accesible y el acceso se controla mediante una de las constantes [de protección de memoria](memory-protection-constants.md). El sistema inicializa y carga cada página confirmada en la memoria física solo durante el primer intento de lectura o escritura en esa página. Cuando finaliza el proceso, el sistema libera el almacenamiento de las páginas confirmadas. <br/> Un proceso puede usar [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) para confirmar páginas físicas de una región reservada. También pueden reservar y confirmar páginas simultáneamente.<br/> Las [**funciones GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) y [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) asignan páginas asignadas con acceso de lectura y escritura.<br/> |



 

 

 
