---
description: 'Paso 2: Agregar un comando de menú para agarrar un marco de póster'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Paso 2: Agregar un comando de menú para agarrar un marco de póster'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282ba112a9035edd9e75c9ea28709ec9c5dc137562ec75dbc5121de04dad864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650905"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>Paso 2: Agregar un comando de menú para agarrar un marco de póster

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Este tema es el paso 2 de [La captura de un marco de póster.](grabbing-a-poster-frame.md)

A continuación, agregue un comando para que el usuario tome un marco de póster de un archivo. Cree un elemento de menú con un identificador de recurso de IDM \_ BITMAP y agregue la siguiente instrucción case al procedimiento de ventana:


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



La función DoShowBitmap devolverá el búfer asignado en *pbmi*. Suponiendo que la función se realiza correctamente, la dirección del mapa de bits (


```C++
pBuffer
```



) se puede calcular como un desplazamiento desde *pbmi*. En la función DoShowBitmap, muestre un cuadro de diálogo Abrir archivo para que el usuario elija un archivo y, a continuación, llame a la función GetBitmap definida por la aplicación, que recuperará el mapa de bits: 


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



Siguiente: [Paso 3: Implementar la Frame-Grabbing función](step-3--implement-the-frame-grabbing-function.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de un marco de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



