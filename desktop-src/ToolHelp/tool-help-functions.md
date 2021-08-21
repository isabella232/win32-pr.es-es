---
title: Funciones de ayuda de herramientas
description: Enumera las funciones de la biblioteca de ayuda de herramientas.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73cc425f415c9cea8af9290743fb1afbb51182f8c03e7ec087ca95948fd2ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058226"
---
# <a name="tool-help-functions"></a>Funciones de ayuda de herramientas

Las siguientes funciones forman parte de la biblioteca de ayuda de herramientas.



| Función                                                           | Descripción                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Toma una instantánea de los procesos especificados, así como de los montones, módulos y subprocesos utilizados por estos procesos. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Recupera información sobre el primer bloque de un montón asignado por un proceso.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Recupera información sobre el primer montón asignado por un proceso especificado.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Recupera información sobre el siguiente montón asignado por un proceso.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Recupera información sobre el siguiente bloque de un montón asignado por un proceso.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Recupera información sobre el primer módulo asociado a un proceso.                                          |
| [**Module32Siguiente**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Recupera información sobre el siguiente módulo asociado a un proceso o subproceso.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Recupera información sobre el primer proceso encontrado en una instantánea del sistema.                                  |
| [**Process32Siguiente**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Recupera información sobre el siguiente proceso registrado en una instantánea del sistema.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Recupera información sobre el primer subproceso de cualquier proceso encontrado en una instantánea del sistema.                    |
| [**Thread32Siguiente**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Recupera información sobre el siguiente subproceso de cualquier proceso encontrado en la instantánea de memoria del sistema.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Copia la memoria asignada a otro proceso en un búfer proporcionado por la aplicación.                                  |



 

 

 




