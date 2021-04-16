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
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Paso 4: dibujo del mapa de bits en el área cliente

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Este tema es el paso 4 de [capturar un fotograma de póster](grabbing-a-poster-frame.md).

El paso final consiste en dibujar el mapa de bits en el área cliente de la ventana de la aplicación mediante la función [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) . En este ejemplo se dibuja simplemente el mapa de bits en la esquina superior izquierda del área cliente, sin tener en cuenta el tamaño de la ventana:


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



Las variables *pBuffer* y *PBMI* se declaran en el [paso 1: crear Windows Framework](step-1--create-the-windows-framework.md)y sus valores se obtienen en [el paso 3: implementar la función Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captación de un fotograma de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
