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
# <a name="using-named-objects"></a>Usar objetos con nombre

En el ejemplo siguiente se muestra el uso de [nombres de objeto](object-names.md) mediante la creación y apertura de una exclusión mutua con nombre.

## <a name="first-process"></a>Primer proceso

El primer proceso utiliza la función [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para crear el objeto mutex. Tenga en cuenta que esta función se realiza correctamente aunque haya un objeto existente con el mismo nombre.


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



## <a name="second-process"></a>Segundo proceso

El segundo proceso utiliza la función [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) para abrir un identificador de la exclusión mutua existente. Esta función genera un error si no existe un objeto mutex con el nombre especificado. El parámetro de acceso solicita acceso completo al objeto de exclusión mutua, que es necesario para que el identificador se use en cualquiera de las funciones de espera.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Nombres de objeto](object-names.md)
</dt> <dt>

[Usar objetos mutex](using-mutex-objects.md)
</dt> </dl>

 

 
