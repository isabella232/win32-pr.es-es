---
description: En el ejemplo siguiente se muestra el uso de nombres de objeto mediante la creación y apertura de una exclusión mutua con nombre.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Usar objetos con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e31d21af713a28d5bee501349e818327750cba15a961ebd0f6a5295be91e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765134"
---
# <a name="using-named-objects"></a>Usar objetos con nombre

En el ejemplo siguiente se muestra el uso de nombres [de objeto](object-names.md) mediante la creación y apertura de una exclusión mutua con nombre.

## <a name="first-process"></a>Primer proceso

El primer proceso usa la [**función CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para crear el objeto mutex. Tenga en cuenta que esta función se realiza correctamente incluso si hay un objeto existente con el mismo nombre.


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

El segundo proceso usa la [**función OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) para abrir un identificador para la exclusión mutua existente. Se produce un error en esta función si no existe un objeto de exclusión mutua con el nombre especificado. El parámetro access solicita acceso completo al objeto mutex, que es necesario para que el identificador se utilice en cualquiera de las funciones de espera.


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

 

 
