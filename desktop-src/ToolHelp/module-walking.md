---
title: Recorrido de módulos
description: Una instantánea que incluye la lista de módulos para un proceso especificado contiene información sobre cada módulo, archivo ejecutable o biblioteca de vínculos dinámicos (DLL) que usa el proceso especificado.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliotecas de vínculos dinámicos
- bibliotecas de vínculos dinámicos, enumerar archivos dll
- enumerar
- enumerar, dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149330"
---
# <a name="module-walking"></a>Recorrido de módulos

Una instantánea que incluye la lista de módulos para un proceso especificado contiene información sobre cada módulo, archivo ejecutable o biblioteca de vínculos dinámicos (DLL) que usa el proceso especificado. Puede recuperar información para el primer módulo de la lista mediante la función [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) . Después de recuperar el primer módulo de la lista, puede recuperar información de los módulos siguientes en la lista mediante la función [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) . **Module32First** y **Module32Next** rellenan una estructura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) con información sobre el módulo.

Puede recuperar un código de estado de error extendido para [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) y [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) mediante la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> El identificador de módulo, que se especifica en el miembro **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), solo tiene significado en Windows de 16 bits.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atravesar la lista de módulos](traversing-the-module-list.md)
</dt> </dl>

 

 