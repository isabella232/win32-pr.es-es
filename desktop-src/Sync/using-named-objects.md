---
description: En el ejemplo siguiente se muestra el uso de nombres de objeto mediante la creación y apertura de una exclusión mutua con nombre.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Usar objetos con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667500"
---
# <a name="using-named-objects"></a><span data-ttu-id="3c8b9-103">Usar objetos con nombre</span><span class="sxs-lookup"><span data-stu-id="3c8b9-103">Using Named Objects</span></span>

<span data-ttu-id="3c8b9-104">En el ejemplo siguiente se muestra el uso de [nombres de objeto](object-names.md) mediante la creación y apertura de una exclusión mutua con nombre.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="3c8b9-105">Primer proceso</span><span class="sxs-lookup"><span data-stu-id="3c8b9-105">First Process</span></span>

<span data-ttu-id="3c8b9-106">El primer proceso utiliza la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para crear el objeto mutex.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="3c8b9-107">Tenga en cuenta que esta función se realiza correctamente aunque haya un objeto existente con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="3c8b9-108">Segundo proceso</span><span class="sxs-lookup"><span data-stu-id="3c8b9-108">Second Process</span></span>

<span data-ttu-id="3c8b9-109">El segundo proceso utiliza la función [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) para abrir un identificador de la exclusión mutua existente.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="3c8b9-110">Esta función genera un error si no existe un objeto mutex con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="3c8b9-111">El parámetro de acceso solicita acceso completo al objeto de exclusión mutua, que es necesario para que el identificador se use en cualquiera de las funciones de espera.</span><span class="sxs-lookup"><span data-stu-id="3c8b9-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="3c8b9-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c8b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8b9-113">Nombres de objeto</span><span class="sxs-lookup"><span data-stu-id="3c8b9-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="3c8b9-114">Usar objetos mutex</span><span class="sxs-lookup"><span data-stu-id="3c8b9-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
