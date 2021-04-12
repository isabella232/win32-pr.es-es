---
title: Usar el control de Media Player de Windows en una aplicación de consola
description: Usar el control de Media Player de Windows en una aplicación de consola
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, aplicaciones de consola
- Modelo de objetos de Windows Media Player, aplicaciones de consola
- modelo de objetos, aplicaciones de consola
- Windows Media Player Mobile, aplicaciones de consola
- Control ActiveX de Windows Media Player, aplicaciones de consola
- Control ActiveX móvil de Windows Media Player, aplicaciones de consola
- Control ActiveX, aplicaciones de consola
- inserción de aplicación de consola
- incrustación, aplicaciones de consola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357279"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Usar el control de Media Player de Windows en una aplicación de consola

Puede crear una instancia del objeto COM de Windows Media Player directamente mediante **CoCreateInstance**. Al hacerlo, el objeto **Player** no muestra ninguna interfaz de usuario. Sin embargo, el objeto sigue siendo útil para las tareas que no requieren la interfaz de usuario, como el trabajo con la biblioteca, la reproducción de archivos de audio digital o el acceso a las propiedades del reproductor.

En el ejemplo de código siguiente se muestra un programa de consola simple que muestra la versión de Windows Media Player en un cuadro de mensaje. En el código de ejemplo se utiliza ATL para aprovechar las ventajas de los punteros inteligentes y la clase de cadena **CComBSTR** .


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Media Player de Windows en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




