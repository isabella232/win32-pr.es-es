---
title: Funciones de ayuda de herramientas
description: Muestra las funciones de la biblioteca de ayuda de la herramienta.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076227"
---
# <a name="tool-help-functions"></a>Funciones de ayuda de herramientas

Las siguientes funciones forman parte de la biblioteca de ayuda de la herramienta.



| Función                                                           | Descripción                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Toma una instantánea de los procesos especificados, así como los montones, módulos y subprocesos utilizados por estos procesos. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Recupera información sobre el primer bloque de un montón asignado por un proceso.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Recupera información sobre el primer montón asignado por un proceso especificado.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Recupera información sobre el siguiente montón asignado por un proceso.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Recupera información sobre el siguiente bloque de un montón asignado por un proceso.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Recupera información sobre el primer módulo asociado a un proceso.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Recupera información sobre el siguiente módulo asociado a un proceso o subproceso.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Recupera información sobre el primer proceso encontrado en una instantánea del sistema.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Recupera información sobre el siguiente proceso registrado en una instantánea del sistema.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Recupera información sobre el primer subproceso de cualquier proceso que se encuentre en una instantánea del sistema.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Recupera información sobre el siguiente subproceso de cualquier proceso que se encuentre en la instantánea de memoria del sistema.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Copia la memoria asignada a otro proceso en un búfer proporcionado por la aplicación.                                  |



 

 

 




