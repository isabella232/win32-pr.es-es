---
description: 'Paso 1: crear Windows Framework'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Paso 1: crear Windows Framework'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678090"
---
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="80b0c-103">Paso 1: crear Windows Framework</span><span class="sxs-lookup"><span data-stu-id="80b0c-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="80b0c-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="80b0c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="80b0c-105">Empiece por crear el marco de trabajo básico de una aplicación de Windows, incluidos WinMain y un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="80b0c-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="80b0c-106">La función WinMain no se muestra aquí. Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes del bucle de mensajes para inicializar la biblioteca com y [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) después de que finalice el bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="80b0c-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="80b0c-107">Comience con el siguiente procedimiento de ventana mínimo:</span><span class="sxs-lookup"><span data-stu-id="80b0c-107">Start with the following minimal window procedure:</span></span>


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



<span data-ttu-id="80b0c-108">Cuando se recupera un fotograma de póster desde el detector de medios, devuelve un búfer que contiene una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguido de los bits de la imagen.</span><span class="sxs-lookup"><span data-stu-id="80b0c-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="80b0c-109">Por lo tanto, defina dos variables estáticas en el procedimiento de ventana: *PBMI* mantendrá un puntero a la estructura **BITMAPINFOHEADER** y *pBuffer* mantendrá un puntero al mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="80b0c-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="80b0c-110">La aplicación asignará el búfer en *PBMI* con `new` , por lo que debe eliminar el búfer antes de que se destruya la ventana.</span><span class="sxs-lookup"><span data-stu-id="80b0c-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="80b0c-111">El puntero *pBuffer* se calcula como un desplazamiento de *PBMI*, por lo que no es necesario eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="80b0c-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="80b0c-112">Siguiente: [paso 2: agregar un comando de menú para capturar un fotograma de póster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="80b0c-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="80b0c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80b0c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80b0c-114">Captación de un fotograma de póster</span><span class="sxs-lookup"><span data-stu-id="80b0c-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
