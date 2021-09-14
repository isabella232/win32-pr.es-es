---
title: Heap Lists and Heap Walking
description: Una instantánea que incluye la lista de montones de un proceso especificado contiene información de identificación para cada montón asociado al proceso especificado e información detallada sobre cada montón.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5a9b8d30e2de1bf5ab37de03fdcb3fde663417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890548"
---
# <a name="heap-lists-and-heap-walking"></a>Heap Lists and Heap Walking

Una instantánea que incluye la lista de montones de un proceso especificado contiene información de identificación para cada montón asociado al proceso especificado e información detallada sobre cada montón. Puede recuperar un identificador para el primer montón de la lista de montones mediante la [**función Heap32ListFirst.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) Después de recuperar el primer montón de la lista, puede recorrer la lista de montones para los montones posteriores asociados al proceso mediante la [**función Heap32ListNext.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) **Heap32ListFirst** y **Heap32ListNext** rellenan una estructura [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) con el identificador de proceso, el identificador del montón y las marcas que describen el montón.

Puede recuperar información sobre el primer bloque de un montón mediante la [**función Heap32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) Después de recuperar el primer bloque de un montón, puede recuperar información sobre los bloques subsiguientes del mismo montón mediante la [**función Heap32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) **Heap32First** y **Heap32Next** rellenan una estructura [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) con información para el bloque adecuado de un montón.

Puede recuperar un código de estado de error extendido para [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)y [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) mediante la [**función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

> [!Note]  
> El identificador del montón, que se especifica en el miembro **th32HeapID** de la estructura [**HEAPENTRY32,**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) solo tiene significado para las funciones de ayuda de la herramienta. No es un identificador ni lo pueden hacer otras funciones.

 

 

 