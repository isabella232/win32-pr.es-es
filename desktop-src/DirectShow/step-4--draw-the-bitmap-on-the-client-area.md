---
description: 'Paso 4: Dibujar el mapa de bits en el área de cliente'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Paso 4: Dibujar el mapa de bits en el área de cliente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253e7d8a5b7508d5ae9f27195dbb7d59b30508ff2aacd8ec2713e0f4d6c909f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951794"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Paso 4: Dibujar el mapa de bits en el área de cliente

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Este tema es el paso 4 de [La captura de un marco de póster.](grabbing-a-poster-frame.md)

El último paso consiste en dibujar el mapa de bits en el área cliente de la ventana de la aplicación mediante la [**función SetDIBitsToDevice.**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) Este ejemplo simplemente pinta el mapa de bits en la esquina superior izquierda del área de cliente, sin tener en cuenta el tamaño de la ventana:


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



Las variables *pBuffer* y *pbmi* se declaran en Step [1: Create the Windows Framework](step-1--create-the-windows-framework.md)y sus valores se obtienen en Step [3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de un marco de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
