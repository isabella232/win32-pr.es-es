---
description: 'Paso 1: Creación de Windows Framework'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Paso 1: Creación de Windows Framework'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feba710c8df948e34c0da0ca9e7a1de85622bfae462290cbce3f36777854cb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072519"
---
# <a name="step-1-create-the-windows-framework"></a>Paso 1: Creación de Windows Framework

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Empiece por crear el marco básico de una Windows aplicación, incluido WinMain y un procedimiento de ventana. La función WinMain no se muestra aquí; llame [**a CoInitialize antes**](/windows/win32/api/objbase/nf-objbase-coinitialize) del bucle de mensajes para inicializar la biblioteca COM y [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) después de que se cierre el bucle de mensajes. Comience con el siguiente procedimiento de ventana mínimo:


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



Cuando se recupera un marco de póster del detector de medios, devuelve un búfer que contiene una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguida de los bits de imagen. Por lo tanto, defina dos variables estáticas en el procedimiento de ventana: *pbmi* contendrán un puntero a la estructura **BITMAPINFOHEADER** y *pBuffer* contendrán un puntero al mapa de bits. La aplicación asignará el búfer en *pbmi* mediante , por lo que debe eliminar el búfer antes de `new` que se destruya la ventana. El *puntero pBuffer* se calcula como un desplazamiento de *pbmi,* por lo que no es necesario eliminarlo.

Siguiente: [Paso 2: Agregar un comando de menú para agarrar un marco de póster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de un marco de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
