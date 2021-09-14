---
title: Recorrido del módulo
description: Una instantánea que incluye la lista de módulos para un proceso especificado contiene información sobre cada módulo, archivo ejecutable o biblioteca de vínculos dinámicos (DLL), que usa el proceso especificado.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliotecas de vínculos dinámicos
- bibliotecas de vínculos dinámicos, enumeración de archivos DLL
- enumerar
- enumerating,DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890537"
---
# <a name="module-walking"></a>Recorrido del módulo

Una instantánea que incluye la lista de módulos para un proceso especificado contiene información sobre cada módulo, archivo ejecutable o biblioteca de vínculos dinámicos (DLL), que usa el proceso especificado. Puede recuperar información del primer módulo de la lista mediante la [**función Module32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) Después de recuperar el primer módulo de la lista, puede recuperar información para los módulos posteriores de la lista mediante la [**función Module32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) **Module32First** y **Module32Next** rellenan una [**estructura MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) con información sobre el módulo.

Puede recuperar un código de estado de error extendido [**para Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) y [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) mediante la [**función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

> [!Note]  
> El identificador del módulo, que se especifica en el miembro **th32ModuleID** de [**MODULEENTRY32,**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)solo tiene significado en la Windows de 16 bits.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recorrer la lista de módulos](traversing-the-module-list.md)
</dt> </dl>

 

 