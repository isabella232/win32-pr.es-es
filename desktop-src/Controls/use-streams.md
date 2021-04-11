---
title: Cómo usar secuencias
description: Puede usar secuencias para transferir datos dentro o fuera de un control Rich Edit. Una secuencia se define mediante una estructura EDITSTREAM, que especifica un búfer y una función de devolución de llamada definida por la aplicación.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104149145"
---
# <a name="how-to-use-streams"></a><span data-ttu-id="350b0-104">Cómo usar secuencias</span><span class="sxs-lookup"><span data-stu-id="350b0-104">How to Use Streams</span></span>

<span data-ttu-id="350b0-105">Puede usar secuencias para transferir datos dentro o fuera de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="350b0-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="350b0-106">Una secuencia se define mediante una estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) , que especifica un búfer y una función de devolución de llamada definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="350b0-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="350b0-107">Para leer los datos en un control Rich Edit (es decir, el flujo en los datos), use el mensaje [**\_ secuencia em**](em-streamin.md) .</span><span class="sxs-lookup"><span data-stu-id="350b0-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="350b0-108">El control llama repetidamente a la función de devolución de llamada de la aplicación, que transfiere una parte de los datos en el búfer cada vez.</span><span class="sxs-lookup"><span data-stu-id="350b0-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="350b0-109">Para guardar el contenido de un control Rich Edit (es decir, hacer streaming de los datos), puede usar el mensaje [**\_ STREAMOUT em**](em-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="350b0-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="350b0-110">El control escribe repetidamente en el búfer y, a continuación, llama a la función de devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="350b0-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="350b0-111">Para cada llamada, la función de devolución de llamada guarda el contenido del búfer.</span><span class="sxs-lookup"><span data-stu-id="350b0-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="350b0-112">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="350b0-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="350b0-113">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="350b0-113">Technologies</span></span>

-   [<span data-ttu-id="350b0-114">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="350b0-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="350b0-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="350b0-115">Prerequisites</span></span>

-   <span data-ttu-id="350b0-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="350b0-116">C/C++</span></span>
-   <span data-ttu-id="350b0-117">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="350b0-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="350b0-118">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="350b0-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="350b0-119">Usar una secuencia</span><span class="sxs-lookup"><span data-stu-id="350b0-119">Use a Stream</span></span>

<span data-ttu-id="350b0-120">En el ejemplo de código siguiente se muestra cómo leer un archivo. rtf en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="350b0-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="350b0-121">El identificador de archivo se pasa a la función de devolución de llamada a través del miembro **dwCookie** de la estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="350b0-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="350b0-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="350b0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350b0-123">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="350b0-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="350b0-124">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="350b0-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




