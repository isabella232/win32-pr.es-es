---
title: Cómo usar los controles de barra de progreso
description: En este tema se explica cómo usar una barra de progreso para indicar el progreso de una operación prolongada de análisis de archivos.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995681"
---
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="cb3de-103">Cómo usar los controles de barra de progreso</span><span class="sxs-lookup"><span data-stu-id="cb3de-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="cb3de-104">En este tema se explica cómo usar una barra de progreso para indicar el progreso de una operación prolongada de análisis de archivos.</span><span class="sxs-lookup"><span data-stu-id="cb3de-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cb3de-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="cb3de-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cb3de-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="cb3de-106">Technologies</span></span>

-   [<span data-ttu-id="cb3de-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="cb3de-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cb3de-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cb3de-108">Prerequisites</span></span>

-   <span data-ttu-id="cb3de-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="cb3de-109">C/C++</span></span>
-   <span data-ttu-id="cb3de-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="cb3de-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cb3de-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="cb3de-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="cb3de-112">Crear un control de barra de progreso</span><span class="sxs-lookup"><span data-stu-id="cb3de-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="cb3de-113">En el código de ejemplo siguiente se crea una barra de progreso y se coloca en la parte inferior del área de cliente de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="cb3de-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="cb3de-114">El alto de la barra de progreso se basa en el alto del mapa de bits de las flechas utilizadas en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="cb3de-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="cb3de-115">El intervalo se basa en el tamaño del archivo dividido por 2.048, que es el tamaño de cada "fragmento" de datos que se lee del archivo.</span><span class="sxs-lookup"><span data-stu-id="cb3de-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="cb3de-116">En el ejemplo también se establece un incremento y se hace avanzar la posición actual de la barra de progreso en el incremento después de analizar cada fragmento.</span><span class="sxs-lookup"><span data-stu-id="cb3de-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a><span data-ttu-id="cb3de-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb3de-117">Remarks</span></span>

<span data-ttu-id="cb3de-118">Debe asegurarse de utilizar la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) correctamente para garantizar la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb3de-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="cb3de-119">Por ejemplo, en el código de ejemplo, debe comprobar para asegurarse de que `ReadFile` realmente Lee todos los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="cb3de-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="cb3de-120">Observe también que el cuarto parámetro de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)(( \_ atributos LPSECURITY)**null**: establece los valores de seguridad predeterminados.</span><span class="sxs-lookup"><span data-stu-id="cb3de-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="cb3de-121">Si necesita una configuración de seguridad específica, debe establecer los valores adecuados en los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="cb3de-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="cb3de-122">Llame a **sizeof** para establecer el tamaño correcto de la estructura de **\_ atributos LPSECURITY** .</span><span class="sxs-lookup"><span data-stu-id="cb3de-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="cb3de-123">Para obtener más información, vea [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md).</span><span class="sxs-lookup"><span data-stu-id="cb3de-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb3de-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb3de-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb3de-125">Usar controles de barra de progreso</span><span class="sxs-lookup"><span data-stu-id="cb3de-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="cb3de-126">Consideraciones de seguridad: controles de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="cb3de-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 