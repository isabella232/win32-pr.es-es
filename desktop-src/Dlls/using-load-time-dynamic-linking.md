---
description: Después de crear un archivo DLL, puede utilizar las funciones que define en una aplicación. A continuación se muestra una sencilla aplicación de consola que usa la función allocas exportada desde Myputs.dll (consulte Creación de una biblioteca de Dynamic-Link sencilla).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Usar Load-Time vinculación dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666845"
---
# <a name="using-load-time-dynamic-linking"></a><span data-ttu-id="e692b-104">Usar Load-Time vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="e692b-104">Using Load-Time Dynamic Linking</span></span>

<span data-ttu-id="e692b-105">Después de crear un archivo DLL, puede utilizar las funciones que define en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e692b-105">After you have created a DLL, you can use the functions it defines in an application.</span></span> <span data-ttu-id="e692b-106">A continuación se muestra una sencilla aplicación de consola que usa la función allocas exportada desde Myputs.dll (consulte [creación de una biblioteca de Dynamic-Link sencilla](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="e692b-106">The following is a simple console application that uses the myPuts function exported from Myputs.dll (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span>

<span data-ttu-id="e692b-107">Dado que en este ejemplo se llama a la función DLL explícitamente, el módulo de la aplicación debe vincularse a la biblioteca de importación. lib.</span><span class="sxs-lookup"><span data-stu-id="e692b-107">Because this example calls the DLL function explicitly, the module for the application must be linked with the import library Myputs.lib.</span></span> <span data-ttu-id="e692b-108">Para obtener más información acerca de la compilación de archivos dll, consulte la documentación que se incluye con las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="e692b-108">For more information about building DLLs, see the documentation included with your development tools.</span></span>


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="e692b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e692b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e692b-110">Vinculación dinámica en tiempo de carga</span><span class="sxs-lookup"><span data-stu-id="e692b-110">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
</dt> </dl>

 

 



