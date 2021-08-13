---
description: Puede usar el mismo archivo DLL en la vinculación dinámica en tiempo de carga y en tiempo de ejecución.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Uso Run-Time dynamic linking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255985"
---
# <a name="using-run-time-dynamic-linking"></a>Uso Run-Time dynamic linking

Puede usar el mismo archivo DLL en la vinculación dinámica en tiempo de carga y en tiempo de ejecución. En el ejemplo siguiente se usa [**la función LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para obtener un identificador del archivo DLL de Myputs (vea Creación de una biblioteca de Dynamic-Link [sencilla).](creating-a-simple-dynamic-link-library.md) Si **LoadLibrary** se realiza correctamente, el programa usa el identificador devuelto en la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener la dirección de la función myPuts del archivo DLL. Después de llamar a la función DLL, el programa llama a [**la función FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para descargar el archivo DLL.

Dado que el programa usa la vinculación dinámica en tiempo de ejecución, no es necesario vincular el módulo con una biblioteca de importación para el archivo DLL.

En este ejemplo se muestra una diferencia importante entre la vinculación dinámica en tiempo de ejecución y la vinculación dinámica en tiempo de carga. Si el archivo DLL no está disponible, la aplicación que usa la vinculación dinámica en tiempo de carga simplemente debe finalizar. Sin embargo, el ejemplo de vinculación dinámica en tiempo de ejecución puede responder al error.


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

 

 
