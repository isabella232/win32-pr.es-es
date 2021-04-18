---
description: Puede usar el mismo archivo DLL en la vinculación dinámica en tiempo de carga y en tiempo de ejecución.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Usar Run-Time vinculación dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d6ca65c510433350b81a282d8bf7a3a3825ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687288"
---
# <a name="using-run-time-dynamic-linking"></a>Usar Run-Time vinculación dinámica

Puede usar el mismo archivo DLL en la vinculación dinámica en tiempo de carga y en tiempo de ejecución. En el ejemplo siguiente se usa la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para obtener un identificador para el archivo dll allocas (consulte [creación de una biblioteca de Dynamic-Link sencilla](creating-a-simple-dynamic-link-library.md)). Si **LoadLibrary** se realiza correctamente, el programa utiliza el controlador devuelto en la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener la dirección de la función puts de la dll. Después de llamar a la función DLL, el programa llama a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para descargar el archivo dll.

Dado que el programa usa la vinculación dinámica en tiempo de ejecución, no es necesario vincular el módulo con una biblioteca de importación para el archivo DLL.

Este ejemplo muestra una diferencia importante entre la vinculación dinámica en tiempo de ejecución y en tiempo de carga. Si el archivo DLL no está disponible, la aplicación que usa la vinculación dinámica en tiempo de carga debe finalizar simplemente. El ejemplo de vinculación dinámica en tiempo de ejecución, sin embargo, puede responder al error.


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vinculación dinámica en tiempo de ejecución](run-time-dynamic-linking.md)
</dt> </dl>

 

 
