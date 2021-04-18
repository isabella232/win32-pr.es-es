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
# <a name="using-run-time-dynamic-linking"></a><span data-ttu-id="10cf3-103">Usar Run-Time vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="10cf3-103">Using Run-Time Dynamic Linking</span></span>

<span data-ttu-id="10cf3-104">Puede usar el mismo archivo DLL en la vinculación dinámica en tiempo de carga y en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="10cf3-104">You can use the same DLL in both load-time and run-time dynamic linking.</span></span> <span data-ttu-id="10cf3-105">En el ejemplo siguiente se usa la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para obtener un identificador para el archivo dll allocas (consulte [creación de una biblioteca de Dynamic-Link sencilla](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="10cf3-105">The following example uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to get a handle to the Myputs DLL (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span> <span data-ttu-id="10cf3-106">Si **LoadLibrary** se realiza correctamente, el programa utiliza el controlador devuelto en la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener la dirección de la función puts de la dll.</span><span class="sxs-lookup"><span data-stu-id="10cf3-106">If **LoadLibrary** succeeds, the program uses the returned handle in the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the address of the DLL's myPuts function.</span></span> <span data-ttu-id="10cf3-107">Después de llamar a la función DLL, el programa llama a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para descargar el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="10cf3-107">After calling the DLL function, the program calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function to unload the DLL.</span></span>

<span data-ttu-id="10cf3-108">Dado que el programa usa la vinculación dinámica en tiempo de ejecución, no es necesario vincular el módulo con una biblioteca de importación para el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="10cf3-108">Because the program uses run-time dynamic linking, it is not necessary to link the module with an import library for the DLL.</span></span>

<span data-ttu-id="10cf3-109">Este ejemplo muestra una diferencia importante entre la vinculación dinámica en tiempo de ejecución y en tiempo de carga.</span><span class="sxs-lookup"><span data-stu-id="10cf3-109">This example illustrates an important difference between run-time and load-time dynamic linking.</span></span> <span data-ttu-id="10cf3-110">Si el archivo DLL no está disponible, la aplicación que usa la vinculación dinámica en tiempo de carga debe finalizar simplemente.</span><span class="sxs-lookup"><span data-stu-id="10cf3-110">If the DLL is not available, the application using load-time dynamic linking must simply terminate.</span></span> <span data-ttu-id="10cf3-111">El ejemplo de vinculación dinámica en tiempo de ejecución, sin embargo, puede responder al error.</span><span class="sxs-lookup"><span data-stu-id="10cf3-111">The run-time dynamic linking example, however, can respond to the error.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="10cf3-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10cf3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10cf3-113">Vinculación dinámica en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="10cf3-113">Run-Time Dynamic Linking</span></span>](run-time-dynamic-linking.md)
</dt> </dl>

 

 
