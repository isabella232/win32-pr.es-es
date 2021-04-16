---
title: Recorrido de subprocesos
description: Una instantánea que incluye la lista de subprocesos contiene información acerca de cada subproceso de cada uno de los procesos que se están ejecutando actualmente.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerar
- enumerar, subprocesos
- subprocesos
- subprocesos, enumerar subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685759"
---
# <a name="thread-walking"></a>Recorrido de subprocesos

Una instantánea que incluye la lista de subprocesos contiene información acerca de cada subproceso de cada uno de los procesos que se están ejecutando actualmente. Puede recuperar información para el primer subproceso de la lista mediante la función [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) . Después de recuperar el primer subproceso de la lista, puede recuperar información de subprocesos posteriores mediante la función [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) . **Thread32First** y **Thread32Next** rellenan una estructura [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) con información sobre los subprocesos individuales de la instantánea.

Puede enumerar los subprocesos de un proceso específico tomando una instantánea que incluye los subprocesos y, a continuación, atravesar la lista de subprocesos, manteniendo la información sobre los subprocesos que tienen el mismo identificador de proceso que el proceso especificado.

Puede recuperar un código de estado de error extendido para [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) y [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) mediante la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> El contenido del miembro **th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) es un identificador de subproceso y se puede usar en cualquier función que requiera un identificador de subproceso.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atravesar la lista de subprocesos](traversing-the-thread-list.md)
</dt> </dl>

 

 