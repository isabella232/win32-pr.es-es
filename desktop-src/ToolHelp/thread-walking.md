---
title: Recorrido por subprocesos
description: Una instantánea que incluye la lista de subprocesos contiene información sobre cada subproceso de cada proceso que se está ejecutando actualmente.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerar
- enumerating,threads
- subprocesos
- threads,enumerating threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890521"
---
# <a name="thread-walking"></a>Recorrido por subprocesos

Una instantánea que incluye la lista de subprocesos contiene información sobre cada subproceso de cada proceso que se está ejecutando actualmente. Puede recuperar información para el primer subproceso de la lista mediante la [**función Thread32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) Después de recuperar el primer subproceso de la lista, puede recuperar información para subprocesos posteriores mediante la [**función Thread32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) **Thread32First** y **Thread32Next** rellenan una [**estructura THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) con información sobre subprocesos individuales en la instantánea.

Puede enumerar los subprocesos de un proceso específico tomando una instantánea que incluya los subprocesos y, a continuación, recorriendo la lista de subprocesos, manteniendo información sobre los subprocesos que tienen el mismo identificador de proceso que el proceso especificado.

Puede recuperar un código de estado de error extendido para [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) y [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) mediante la [**función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

> [!Note]  
> El contenido del **miembro th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) es un identificador de subproceso y puede ser utilizado por cualquier función que requiera un identificador de subproceso.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recorrer la lista de subprocesos](traversing-the-thread-list.md)
</dt> </dl>

 

 