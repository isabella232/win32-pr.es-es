---
description: Una acción personalizada puede llamar a una función definida en una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Bibliotecas de Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082781"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="664e9-103">Bibliotecas de Dynamic-Link (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="664e9-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="664e9-104">Una acción personalizada puede llamar a una función definida en una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.</span><span class="sxs-lookup"><span data-stu-id="664e9-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="664e9-105">La DLL puede existir como un archivo instalado durante la instalación actual o como una secuencia binaria temporal que se origina en la [tabla binaria](binary-table.md) de la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="664e9-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="664e9-106">Tenga en cuenta que todas las funciones llamadas, incluidas las acciones personalizadas en archivos dll, deben especificar la \_ \_ Convención de llamada Stdcall.</span><span class="sxs-lookup"><span data-stu-id="664e9-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="664e9-107">Por ejemplo, para llamar a CustomAction, use lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="664e9-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="664e9-108">Para obtener más información, vea [obtener acceso a la sesión del instalador actual desde una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md) .</span><span class="sxs-lookup"><span data-stu-id="664e9-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="664e9-109">Los siguientes tipos de acciones personalizadas llaman a una biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="664e9-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="664e9-110">Tipo de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="664e9-110">Custom action type</span></span>                                 | <span data-ttu-id="664e9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="664e9-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="664e9-112">Tipo de acción personalizada 1</span><span class="sxs-lookup"><span data-stu-id="664e9-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="664e9-113">Archivo DLL almacenado en un flujo de tabla binaria.</span><span class="sxs-lookup"><span data-stu-id="664e9-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="664e9-114">Tipo de acción personalizada 17</span><span class="sxs-lookup"><span data-stu-id="664e9-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="664e9-115">Archivo DLL instalado con un producto.</span><span class="sxs-lookup"><span data-stu-id="664e9-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="664e9-116">Para utilizar COM, debe llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) en la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="664e9-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="664e9-117">No salga si observa que el subproceso ya se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="664e9-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="664e9-118">Por ejemplo, el subproceso se inicializa en una instalación por equipo, pero no en una instalación por usuario.</span><span class="sxs-lookup"><span data-stu-id="664e9-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="664e9-119">Vea [lista de Resumen de todos los tipos de acciones personalizadas](summary-list-of-all-custom-action-types.md) para obtener un resumen de todos los tipos de acciones personalizadas y cómo se codifican en la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="664e9-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
