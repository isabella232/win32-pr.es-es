---
title: Recorrido del proceso
description: Una instantánea que incluye la lista de procesos contiene información sobre cada proceso que se está ejecutando actualmente.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerar
- enumerating,processes
- procesos
- procesos, enumeración de procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890532"
---
# <a name="process-walking"></a>Recorrido del proceso

Una instantánea que incluye la lista de procesos contiene información sobre cada proceso que se está ejecutando actualmente. Puede recuperar información para el primer proceso de la lista mediante la [**función Process32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) Después de recuperar el primer proceso de la lista, puede recorrer la lista de procesos para las entradas posteriores mediante la [**función Process32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) **Process32First y** **Process32Next** rellenan una [**estructura PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) con información sobre un proceso en la instantánea. Para obtener un ejemplo, vea [Tomar una instantánea y Ver procesos](taking-a-snapshot-and-viewing-processes.md).

Puede recuperar un código de estado de error extendido [**para Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) y [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) mediante la [**función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Puede leer la memoria de un proceso específico en un búfer mediante la función [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (o la [**función VirtualQueryEx).**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex)

> [!Note]  
> El contenido de los miembros **th32ProcessID** y **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) son identificadores de proceso y pueden ser utilizados por cualquier función que requiera un identificador de proceso.

 

 

 