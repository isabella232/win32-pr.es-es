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
# <a name="step-1-create-the-windows-framework"></a>Paso 1: crear Windows Framework

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Empiece por crear el marco de trabajo básico de una aplicación de Windows, incluidos WinMain y un procedimiento de ventana. La función WinMain no se muestra aquí. Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes del bucle de mensajes para inicializar la biblioteca com y [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) después de que finalice el bucle de mensajes. Comience con el siguiente procedimiento de ventana mínimo:


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



Cuando se recupera un fotograma de póster desde el detector de medios, devuelve un búfer que contiene una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguido de los bits de la imagen. Por lo tanto, defina dos variables estáticas en el procedimiento de ventana: *PBMI* mantendrá un puntero a la estructura **BITMAPINFOHEADER** y *pBuffer* mantendrá un puntero al mapa de bits. La aplicación asignará el búfer en *PBMI* con `new` , por lo que debe eliminar el búfer antes de que se destruya la ventana. El puntero *pBuffer* se calcula como un desplazamiento de *PBMI*, por lo que no es necesario eliminarlo.

Siguiente: [paso 2: agregar un comando de menú para capturar un fotograma de póster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captación de un fotograma de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
