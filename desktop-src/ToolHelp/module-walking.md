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
# <a name="module-walking"></a><span data-ttu-id="f8428-107">Recorrido de módulos</span><span class="sxs-lookup"><span data-stu-id="f8428-107">Module Walking</span></span>

<span data-ttu-id="f8428-108">Una instantánea que incluye la lista de módulos para un proceso especificado contiene información sobre cada módulo, archivo ejecutable o biblioteca de vínculos dinámicos (DLL) que usa el proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="f8428-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="f8428-109">Puede recuperar información para el primer módulo de la lista mediante la función [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) .</span><span class="sxs-lookup"><span data-stu-id="f8428-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="f8428-110">Después de recuperar el primer módulo de la lista, puede recuperar información de los módulos siguientes en la lista mediante la función [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) .</span><span class="sxs-lookup"><span data-stu-id="f8428-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="f8428-111">**Module32First** y **Module32Next** rellenan una estructura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) con información sobre el módulo.</span><span class="sxs-lookup"><span data-stu-id="f8428-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="f8428-112">Puede recuperar un código de estado de error extendido para [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) y [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) mediante la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f8428-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="f8428-113">El identificador de módulo, que se especifica en el miembro **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), solo tiene significado en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f8428-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f8428-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8428-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8428-115">Atravesar la lista de módulos</span><span class="sxs-lookup"><span data-stu-id="f8428-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 