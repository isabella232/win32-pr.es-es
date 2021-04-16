---
description: 'Paso 4: dibujo del mapa de bits en el área cliente'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Paso 4: dibujo del mapa de bits en el área cliente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424083"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="06855-103">Paso 4: dibujo del mapa de bits en el área cliente</span><span class="sxs-lookup"><span data-stu-id="06855-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="06855-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="06855-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="06855-105">Este tema es el paso 4 de [capturar un fotograma de póster](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="06855-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="06855-106">El paso final consiste en dibujar el mapa de bits en el área cliente de la ventana de la aplicación mediante la función [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) .</span><span class="sxs-lookup"><span data-stu-id="06855-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="06855-107">En este ejemplo se dibuja simplemente el mapa de bits en la esquina superior izquierda del área cliente, sin tener en cuenta el tamaño de la ventana:</span><span class="sxs-lookup"><span data-stu-id="06855-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



<span data-ttu-id="06855-108">Las variables *pBuffer* y *PBMI* se declaran en el [paso 1: crear Windows Framework](step-1--create-the-windows-framework.md)y sus valores se obtienen en [el paso 3: implementar la función Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).</span><span class="sxs-lookup"><span data-stu-id="06855-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06855-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06855-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06855-110">Captación de un fotograma de póster</span><span class="sxs-lookup"><span data-stu-id="06855-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
