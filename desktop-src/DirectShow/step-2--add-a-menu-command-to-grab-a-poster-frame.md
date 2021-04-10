---
description: 'Paso 2: agregar un comando de menú para capturar un fotograma de póster'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Paso 2: agregar un comando de menú para capturar un fotograma de póster'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156736"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>Paso 2: agregar un comando de menú para capturar un fotograma de póster

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Este tema es el paso 2 de [capturar un fotograma de póster](grabbing-a-poster-frame.md).

A continuación, agregue un comando para que el usuario obtenga un fotograma de póster de un archivo. Cree un elemento de menú con un identificador de recurso de mapa de bits de IDM \_ y agregue la siguiente instrucción Case al procedimiento de ventana:


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



La función DoShowBitmap devolverá el búfer asignado en *PBMI*. Suponiendo que la función se realiza correctamente, la dirección del mapa de bits (


```C++
pBuffer
```



) se puede calcular como un desplazamiento desde *PBMI*. En la función DoShowBitmap, muestre un cuadro de diálogo **Abrir archivo** para que el usuario elija un archivo y, a continuación, llame a la función GetBitmap definida por la aplicación, que recuperará el mapa de bits:


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



Siguiente: [paso 3: implementar la función Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captación de un fotograma de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



